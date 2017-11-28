

### Create Project Strcture

```sh
mkdir learnnpm
cd learnnpm/
mkdir app
touch package.json
echo "{ }" > package.json
```

##### Install npm depedencies

```shell
npm install --save jquery
```

after installing npm dependencies make sure your package.json looks like below: 

```json
{
    "dependencies": {
        "jquery": "^3.2.1"
    }
}

```

also verify there is a folder named node_modules created with jquery dependency added to it. 

##### Using npm libary 

```shell
touch index.html
```

Let's use the jquery dependency we installed using npm in our html file. 

```html
<html>
    <head>
        <script src="./../node_modules/jquery/dist/jquery.js" ></script>
        <script>
            $(document).ready(function(){
                $('#btn').click(function(){
                    alert('Hi...');
                });
            });
        </script>
    </head>
    <body>
        <button id="btn">Click Me</button>
    </body>
</html>
```

The above code is trivial, the only line to pay attention is: 

```html
<script src="./../node_modules/jquery/dist/jquery.js" ></script>
```

 This should include the latest jquery version (3.2.1) installed by npm in your html file. 

Access this html file in browser, A simple alert can be seen clicking on `Click me ` button. 



Congrats !! you have learnt how to manage your front-end depedencies using `NPM` 