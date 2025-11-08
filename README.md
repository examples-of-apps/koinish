# koinish

Minimalist digital design inspired by Koin.

## API

```ts
import {
  module, modules, singleOf, factoryOf, startDI, inject, t, override
} from 'koinish';

// di/modules.ts
const appModule = module(
    singleOf(WeatherService),
    singleOf(MyRepository),
);

// main.ts
startDI(modules(appModule));

// em qualquer lugar
const svc = inject(WeatherService);

```