# mems
# Multiple selection 
 <tr *ngFor="let cameraPreset of savedCamArray; let i = index">
                            <td scope="row">{{ i+1  }}</td>
                            <td scope="row">

                                <div>{{ cameraPreset.camObject.name  }}</div>
                                <div class="preset-value">{{ cameraPreset.preset  }}</div>

                            </td>
                            <td> <mat-checkbox  [checked]="checkedTimeSlot[i] === i + 'x'" (change)="checkedTimeSlot[i] = i+'x'">Default</mat-checkbox>
                                    <mat-checkbox  [checked]="checkedTimeSlot[i] === i + 'y'" (change)="checkedTimeSlot[i] = i+'y'"   > </mat-checkbox> <span class="cust-input">
                                        Custom: <input  numericDirective numericType="number" [attr.disabled]="checkedTimeSlot == 0 ? '' : null" type="text" class="custom-value" value="10"> </span>
                                    
                                </td>
                            
                            <td> <i (click)="deletePresetObject(i)"  class="its-rubbish-bin-1"></i>
                            </td>
                        </tr>

# .ts file checkedTimeSlot: any = [];
