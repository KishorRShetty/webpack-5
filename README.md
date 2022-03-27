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

multiple files are genereated with this if there more entries in the entry object

## Loaders => images, js, css, saas: webpack Compiles them
npm i -D sass style-loader sass-loader css-loader
import the css

add a module object and rules arrayoob in wc.js
add a regex to detect the extension /\.scss$/

## HTML plugin : plugin's are more powerful.
we can delete the whole dist folder and have a template
npm run build wil create everything
npm i -D html-webpack-plugin
const require html-webpack-plugin

create a plugin array -> HtmlwebPackPlugin takes {}
{} can have the title of the page ..

now we can delete the dist and everything will be created on build

## Add a template to persist the html
build will replace the html otherwise
remove the script
we can use <%=htmlWebpackPlugon.options.[] %> to access the template values
<title><%=htmlWebpackPlugin.options.title %></title>
