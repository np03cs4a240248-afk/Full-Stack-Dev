# Workshop 2 – MVC and DRY

Based on the provided Workshop 2 PDF and the existing Workshop 1 application. The uploaded project already had controllers, resource routes, and model binding; these were preserved. Student validation is shared in `rules(?Student $student)` and Course validation in `rules()`. Shared component layout, navbar, footer, alert, fields, delete form, and Student form have been added. Course form remains a reusable Blade partial.

The PDF mixes component-based layouts in Steps 13–14 with legacy `@extends` in Step 15. This implementation consistently uses `<x-layouts.app>` for both resources.

## Run locally

1. `composer install`
2. Copy `.env.example` to `.env`, configure database connection.
3. `php artisan key:generate`
4. `php artisan migrate`
5. `php artisan serve`
6. Visit `/students` and `/courses`.

Check both resources' create/view/edit/delete flows, duplicate student email validation, invalid input, navbar, footer, and missing record 404. Dependencies, MySQL and HTTP flows were not run in the build environment.
