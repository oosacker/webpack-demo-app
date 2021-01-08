# webpack-demo-app
Accompanies my 10-part Youtube Webpack course.  Each commit comes with detailed notes.

https://www.youtube.com/watch?v=MpGLUVbqoYQ&t=35s

https://webpack.js.org/guides/getting-started/#basic-setup

npm install webpack webpack-cli --save-dev

* Has a common webpack setting plus production and dev ones, select one by the build/start script. 

* webpack-dev-server will NOT generate files inside dist/

* Add hash to the js to make browser redownload them (cache-busting - only for production build): [contentHash] or [hash]. The filename of the assets will be changed with the hash, so use the HTML plugin to generate HTML from a template (HtmlWebpackPlugin). 

* Also have to use file-loader for images etc

* If no config, by default webpack will combine all js files to single js inside dist/

* Removes old dist/ files with clean-webpack-plugin

* By default the CSS code is inside the compiled js and injected to html as <style>. This is slow to load as js files are loaded at the bottom of the html. So CSS should be in a separate file in production using MiniCssExtractPlugin


