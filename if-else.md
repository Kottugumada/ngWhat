## If-Else In Angular
As of Angular 4.0.0 if else at the block level implementation has become so much more easier.
 
 ` 
    <div *ngIf="isValid;else other_content">if block content here... </div>`
   
   `<ng-template #other_content>else block content here...</ng-template>`
    Here is a working Plunkr demo: https://embed.plnkr.co/hmpYOCgy7EogtjStunEv/

