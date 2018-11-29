<h1>React Development</h1>
  <p>When you want to work with react material version, go to inside the folder and run <strong>nmp i</strong> , then run <strong>'npm start'</strong> for starting development server, and run <strong>'gulp'</strong> or 'npm run styles' for scss compilation for your style change. React app should start with server <strong>localhost:3000</strong>. If you want to build a production verison of react app, please run <strong>'npm run build'</strong> command, it will create a build folder inside react-material folder fro you and put this build folder on any server like and see the optimize app version.</p>
  
<p>React Material admin app created with create-react-app cli so first when you will go to the react-material folder you will find the structure like first image above.</p>
<ul>
  <li><b>build</b> - Production ready version inside it, you can run 'npm run build' to create your own customize version</li>
  <li><b>public</b> - This folder serve index.html file while development mode.</li>
  <li><b>src</b> - This is the main folder for your development.</li>
  <li><b>gulpfile.babel.js</b> - File responsible for scss compiling task</li>
</ul>

<p>When you got inside src folder of react-material design. You will see the structure like the second image above. Let me write a quick details for each folder of src/.</p>

<ul>
  <li><b>actions</b> - Folder for every action happens in this app using redux.</li>
  <li><b>charts</b> - You will find all chart component inside this folder</li>
  <li><b>components</b> - Inside this folder you will find all stateless component and according to redux so called dump component. Some component have some logic.</li>
  <li><b>containers</b> - Folder represent all the component which called smart component to communicate with redux store</li>
  <li><b>img</b> - All image used to builld this app</li>
  <li><b>pages</b> - This folder resresent all the routes pages. Basically inside this folder compmonent only for creating route page and structure those page using components folder all component.</li>

  <li><b>reducers</b> - Folder contains all redux store files.</li>
  <li><b>routers</b> - This folder serve app routes and a parent component which is serve from App.js file, please look colosely routers.js file.</li>
  <li><b>sass</b> - All scss file inside it.</li>
  <li><b>style-switcher</b> - Represent the style switcher component.</li>
</ul>

<h6>Theming with react material</h6>

<p>This seciton briefly describe which file you change to make your own color template.Right now sidebar background color, header left side background, header top bar background colors are dynamically changed via redux store. If you want to change this three dynamic section background color, you can do it manually by visiting those file
</p>
<code>
  header.js ( header top bar bg)</br>
  routers.js ( header left side and sidebar bg)</br>
  You will see those lines on header.js file as well as routers.js file similar kind of implementation.</br>

  const style = {</br>
    background: this.props.colorHeaderBanner.color</br>
  }
</code>


<p><mark>All you need to set a color property for background.</mark></p>

<p>Now for material color scheme changing option

On App.js file you will see those lines</p>
<code>
  const muiTheme = getMuiTheme({</br>
    palette: {</br>
      primary1Color: '#258df2',</br>
      accent1Color: '#40c741',</br>
    }
  });
</code>


<p>This is responsible for the material default theme color. You can change those color if you don't want material color scheme thats used for this template.

And the final part for default template color that i used for my own choice.
My custom used color cames from 'src/sass/_variables.scss' file.

If you look on _variables.scss file you will easily understand the variable name and what purpose this variable serve. For example those lines</p>
<code>
  $color-primary: #258df2;</br>
  $color-primary-hover: darken($color-primary, 10%);</br>
  $color-secondary: #40c741;</br>
  $color-body-bg: #fbfcfd;</br>
  $color-bg-white: #fff;</br>

  $color-warning: #fdba2c;</br>

  $color-danger: #e64043;</br>

  $color-green: #2bcdbd;</br>
  $color-purple: #e884f9;</br>
</code>

</br></br>


<p>These are the custom colors, you can change anything from here and see the change on browser.</p>
<p>For other style option change you will find insdie sass folder named based on their class name and relevent to the react component, hope you will find easily.</p>  
