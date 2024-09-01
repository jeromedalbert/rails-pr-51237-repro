# Minimal example app

### Steps to repro

1. Run the following commands:

    ```
    bin/setup
    bin/rails server
    ```

1. Go to http://127.0.0.1:3000/posts/new
1. Check the page source code, search for the word "namespace"
1. Observe that the input tag has `id="namespace_blah"` but the label tag has
   `for="blah"` with no prefix.

### How this app was created

```shell
$ rails --version
Rails 7.2.1
$ rails new myapp
$ cd myapp
$ bin/rails generate scaffold post title:string
```
