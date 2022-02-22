# Create-Strapi-App@3 Workaround
There is a known issue with ```npx create-strapi-app``` where the toolchain will fail at the initial shell script ```mkdir``` command if the app is being installed on a path that has a space in any of the directory names. Users whose PCs have been set up for them by a company admin may not be able to remove the offending spaces (for example, if their user folder has been assigned as 'firstname lastname' and they're unable to change it.)   

A version of strapi can be pulled from an image on Dockerhub, however that implementation differs from the codebase that ```create-strapi-app``` produces, so it may not be an appropriate substitute for learners who are trying to follow along with a specific course page or tutorial.  

This repository contains a fresh install of create-strapi-app@3 (version 3, gradually being deprecated but it has simpler data structure and many old tutorials and classes are based on it), along with instructions on how to clone & install dependencies on your local machine.   

TLDR: I ran the toolchain so you don't have to. :)

## How to install

1. Create your app folder

2. Navigate into that app folder in terminal, and clone this repository  
```git clone https://www.github.com/jayeclark/create-strapi-app-3```

3. Ensure you are using node v14.17.0 (this assumes you have nvm installed and have added 14.17.0 as an option -- if you have not added it, you can do so with ```nvm install 14.17.0```)  
```nvm use 14.17.0```

4. Install depedencies (with no optional deps)  
```yarn install --ignore-optional```

5. Run the development server  
```yarn run develop```
