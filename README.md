# Wilson Composer Project

Wilson is the **Access** in-house installation profile and theme starterkit for Drupal 9+. A development kickstarter with a focus on Paragraph-based landing pages.

Use this project with Composer to generate a Wilson Drupal codebase. This is the Wilson equivalent to running `composer create-project drupal/recommended-project`.

## Installation

### For projects that require a `web` webroot

```
composer create-project accessdigital/wilson-project my-project --repository="{\"url\": \"https://github.com/accessdigital/wilson-project\", \"type\": \"vcs\"}" --stability=dev
```

### For projects that require a `docroot` webroot

```
composer create-project accessdigital/wilson-project my-project --no-install --repository="{\"url\": \"https://github.com/accessdigital/wilson-project\", \"type\": \"vcs\"}" --stability=dev
cd my-project
sed -i '' -e 's_web/_docroot/_g' composer.json
mv web docroot
composer install
```

See the full [Wilson installation guide](https://accessdigital.atlassian.net/wiki/spaces/AD/pages/2220916744/Installation+steps) on Confluence.
