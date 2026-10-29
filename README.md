# CoffeeDate

An Android reference project in Kotlin and Jetpack Compose: a coffee planner that pairs colleagues for coffee dates per weekday and lets you search the pairs. It shows an MVVM structure with a network layer, dependency injection and tested ViewModels.

## Architecture

- **Presentation:** Compose screens and a `ViewModel` exposing `StateFlow` state and a separate error flow
- **Domain:** use cases (`GetAllEmployeesUseCase`, `GetCoffeePairListUseCase`, …) returning a shared `Result` type
- **Data:** Retrofit service with Moshi models, mapped to domain models; generic API and error-body parsing (`lib/api`)
- **DI:** Dagger components and modules for the API, OkHttp and Retrofit setup

## Tech stack

Kotlin · Jetpack Compose · Material 3 · MVVM · Coroutines/StateFlow · Dagger · Retrofit · OkHttp · Moshi · JUnit · kotlinx-coroutines-test · Strikt

## Tests

ViewModel unit tests with a coroutine test rule:

```bash
./gradlew :app:testDebugUnitTest
```

## Note

Built as a reference project with an AI assistant in Android Studio as a pair programmer. The backend endpoints it calls are a demo setup, not a public service.
