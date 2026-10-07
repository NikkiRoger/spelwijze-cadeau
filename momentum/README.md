# Indiethos – App (prototype)

Current module: **Momentum**

## Supabase Auth URL configuration

The browser app uses Supabase passwordless email sign-in.

In Supabase Dashboard → **Indiethos - App** → **Authentication** → **URL Configuration** set:

- **Site URL:** `https://nikkiroger.github.io/spelwijze-cadeau/momentum/`
- **Redirect URL:** `https://nikkiroger.github.io/spelwijze-cadeau/momentum/`

The app also passes its current page URL as `emailRedirectTo`.

## Current flow

1. Enter email
2. Receive magic link
3. First login → Artist Compass
4. Save compass
5. Momentum actions load from Supabase
6. “I did it” creates a `momentum_entries` record
7. Monthly count is read from Supabase
8. Returning users skip onboarding

## Backend

Supabase project: **Indiethos - App**

Tables:
- `profiles`
- `artist_compass`
- `actions`
- `momentum_entries`

RLS is enabled on all public tables.
