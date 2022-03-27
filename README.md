## Notes

src and dist in the begining
created html in the dist and js in src and linked the js

## npm init

for import export, we can use type:module in package.json.
webpack will take care of that here.

## install webpack

-D for installing as a dev dependancy
npm i -D webpack webpack-cli

## configuring the webpack

add "build":"webpack" under scripts in the package.json
also add "build":"webpack --mode production" until the webpack.config file is created

## test it

npm run build
index.js was the original file in the src
main.js is created in the dist folder

## Create the webpack.config.js

module.export={} it
add mode:'developement' here and remove --mode production from package.json (webpack will now reference this from now)

## change the default values if required

change the entry, output filename etc in webpack.config.js
default filename is main.js
we made it bundle.js

## we can have multiple entry points ref bundle below
change it to an object

entry:{
    bundle:'',
    name2:''
}
## access them as name
output:{
    filename: [name].js
}

multiple files are genereated with this if there are any in the entry object


