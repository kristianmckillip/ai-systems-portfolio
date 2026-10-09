# Project 07 · Veridian Android

**Status:** Google Play internal beta  
**Platform:** Android  
**Release:** 1 (0.9.0)  
**Beta milestone:** September 28, 2026

## Implementation and beta delivery

Veridian is a to-do application for realistic planning on low-capacity days. Its implementation separates the client’s local storage, an optional AI service, and access to the Android beta.

## Verified stack

The October 8 source inspection identified:

- .NET 10 MAUI clients targeting Windows and Android
- SQLite for local storage
- An ASP.NET Core AI Assist gateway
- Docker deployment on Railway
- PostgreSQL for AI Assist access-code records
- OpenRouter for model generation

## Architecture and boundaries

The MAUI application supplies the client interface and uses SQLite locally. Optional AI Assist runs through a separate server-side gateway connected to OpenRouter.

The gateway uses individually issued access codes with aliases, expiry and quotas. An administrator command-line tool manages issuance and revocation.

Google Play enrollment and AI Assist access are distinct. Adding someone to the Play tester list allows access to the Android beta; it does not itself issue access to the optional AI service. That separation is an important part of operating the beta.

## Build and distribution

Development records include a signed Android app bundle and later device-specific APK/APKS packaging. Google Play Console confirmed release 1 (0.9.0), dated September 28, as available to internal testers; that status was checked again on October 8.

The gateway’s liveness endpoint responded during the October 8 inspection. That confirms a responding process at that time, rather than an end-to-end generation or database test.

## Development approach and my contribution

I shaped requirements, product priorities, scope and testing, with AI-assisted coding supporting implementation. An early decision was to inspect the existing prototype, retain useful work and get the basic application running before investing in polish.

Internal beta distribution supports feedback on installation, first launch, confusing behavior and useful changes. Early tester use has been reported; broader validation is ongoing.

## Evidence still needed

The exact task data model, client-to-gateway request flow, automated-test coverage and specific Android defects resolved need a closer source review.
