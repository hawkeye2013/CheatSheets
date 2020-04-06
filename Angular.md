# Angular Cheat Sheet

This will hold some boilerplate for various angular things

## Boilerplate

### Components

```ts
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'selector-name',
  templateUrl: 'name.component.html',
})
export class NameComponent implements OnInit {
  constructor() {}

  ngOnInit() {}
}
```

### Services

```ts
import { Injectable } from '@angular/core';

@Injectable({ providedIn: 'root' })
export class ServiceNameService {
  constructor() {}
}
```

### Module

```ts
import { NgModule } from '@angular/core';

import { NameComponent } from './name.component';

@NgModule({
  imports: [],
  exports: [],
  declarations: [NameComponent],
  providers: [],
})
export class NameModule {}
```

### Custom Validator

```ts
import {} from '@angular/forms';

export class StockValidators {
  static checkBranch(control: AbstractControl) {
    const regexp = /^[a-z]\d{3}$/i; // Checks for one letter and three numbers
    const valid = regexp.test(control.value);
    return valid ? null : { invalidBranch: true };
  }
}
```
