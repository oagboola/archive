<h1>How I like my meteor app </h1>


<p>`meteor create <name of app>` gives you this layout:</p>

<p>
  <blockquote>
    | app/ <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| .meteor/ <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;....... <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| client/ <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| main.css <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| main.html <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| main.js <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| server/ <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| main.js <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| .gitignore <br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| package.json <br>
  </blockquote>
</p>

<p>
  The `.meteor` folder contains a bunch of stuff you don't really need to meddle with.<br>

  Meteor differentiates the 'frontend' from the 'backend' by the naming of these folders'. The client folder contains everything related to the 'frontend' and the server folder contains everything related to the 'backend'. Folders not within client or server contains stuff that could be either in the front or backend.
</p>

<p>
<h4>
  The client folder <br>
</h4>
  It's very simple to set up the front end of the meteor app, you could actually just create all your html, js and css files in the root of the client folder, everything will be fine, but this won't be good practice, things could get muddled up really fast. You could even just have only one css and one js file, as long as you write your code right, any html file in the client folder is connected to it. All that would be ub the client folder are mostly your html files, the style and javascript connected to it. It would be best to create a folder for each 'component of your app' the have the html, css and js files in that particular folder.

  On the client side, you could have a folder or a single file for your subscriptions, alternatively, subsricption could be done when routing.
</p>

<p>
<h4>
  The server folder <br>
</h4>
  <p>

    The server folder will be a bit more complicated than the client folder, here you may have some configuration and methods. some of the folders you'll need here:
  </p>

  <p>
    <b>Accounts folder:<br></b>
    Here you'll have your accounts configuration such as github login, social media login and local login, you can set up a file for each configuration.
  </p>

  <p>
    <b>Methods</b> <br>
    In order to write methods that can be re-usable in different parts of the app, meteor requires it to be on the server side. You'll need a folder to contain all your methods and individual files for methods relating to particular components of you app
  </p>

  <p>
    <b>Publications</b>: <br>
    You can have all your publications in one file or create individual files for each of them.
  </p>

  Other folders: <br>

  <p>
    <b>Public folder</b> <br>
    This houses your assets which would mostly be images, fonts...etc, meteor will only be able to serve you images if they are contained in the folder, you can have sub-directories to organize your assets but they have to be in the public folder
  </p>

  <p>
    <b>lib folder</b> <br>
    Will contain other files that would be a misfit in any of the above named folders or any other folders you have created, in this folder, you could have your routes, collections or any other files
  </p>

  <p>
    At the end of the day, my meteor app look somewhat like:
    <blockquote>
      | app/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| .meteor/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;....... <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| client/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| products/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| products.css <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| products.html <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| products.js <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| contact/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| contact.css <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| contact.html <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| contact.js <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| subscriptions.js <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| server/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| Accounts_config/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| serviceConfig.js <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| methods/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| contactMethods.js <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| productMethods.js <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| publicatons.js <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| public/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| images/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| lib/ <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| routes.js <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| collections.js <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| main.js <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| .gitignore <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;| package.json <br>
    </blockquote>
  </p>
</p>
