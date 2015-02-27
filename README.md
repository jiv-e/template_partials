# template_partials
Proof of concept module for component based / style guide driven / atomic design Drupal theming.

# Requirements
- Drupal 7
- Developed for and tested with Omega 4 theme.

# Installation
1. Download and enable this module.
2. Download Omega 4 theme.
3. Create a Omega subtheme and set it as
   default theme.

# Usage
1. Create folder called `partials` in your
   Omega subtheme folder.
2. Add a file called `test.inc` inside the
   `partials` folder with this content:
    ```php
    <h1 class="hello">Hello <?php print $user->name;?>!</h1>

    ```
3. Go to `[site-url]/parts/test` to see the
   rendered partial.
4. Create a file `sass/components/_hello.scss` in
   your theme with this content:
    ```sass
    .hello {
      color: red;
    }

    ```
5. Compile sass!
6. Go to `[site-url]/parts/test` to see the
   rendered partial.
7. Copy the `page.tpl.php` file from the
   Omega theme's templates folder to your sub
   themes templates folder.
8. Add this line to someplace in the
   `page.tpl.php` file:
    ```php
    <?php include template_partials_partial('test'); ?>

    ```
9. Go to some page on your site and see the
   rendered result.

# Ok... so what?
This is just a one step towards style guide
driven / atomic design workflow on Drupal.
Maybe you find it interesting and want to
take it forward. The code is ugly and ad
hoc at the moment. If you have any ideas or
pull requests I would be happy to hear from
you!
