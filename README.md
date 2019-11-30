# Loading
Loading functionality for any application with the use of Interceptor.
It is the stand-alone functionality for any application.

# How to use
Copy the "loading" component from app > components > loader
It includes related service and interceptor file

## app.module.ts
Go to app.module.ts and register the service
Add HTTP_INTERCEPTOR in provider

```
import { HTTP_INTERCEPTORS } from '@angular/common/http';
```
```
@NgModule({
  declarations: [
    AppComponent, // along with your other project modules
    LoaderComponent
  ],
  imports: [
    BrowserModule, 
    HttpClientModule
  ],
  providers: [
    {
      provide: HTTP_INTERCEPTORS,
      useClass: LoaderInterceptorService,
      multi: true
    }
  ],
  bootstrap: [AppComponent]
})

```

## app.component.html
```
include <app-loader><app-loader> 
```
