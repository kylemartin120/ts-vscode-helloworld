# ts-vscode-helloworld

Starter configuration for a VSCode TypeScript project. Allows you to transpile TypeScript to JavaScript, run the code, and debug it with breakpoints in one step.

## Required setup

You'll need NodeJS and npm installed; those can be downloaded [here](https://nodejs.org/en/download/). Once that's set up, you'll need to run the following command to install TypeScript:

    npm install -g typescript

You'll also need to install [VSCode](https://code.visualstudio.com/download).

## Opening the project

Open the project in VSCode at the root directory. If the project is opened at a sub-directory, the configuration files that tell VSCode how to build and debug will not be read properly.

## Project structure

The file you will need to edit is `src\main.ts`. Any code that is present there can be compiled, run, and debugged by VSCode. As you add more TypeScript files, you should add them within the `src` directory (feel free to create any subfolders that you need for your own project's organization).

The file `tsconfig.json` (in the root directory) contains basic information about where to put build files, whether to generate a source map, and how to interpret the eventual JS code. Within the `.vscode` directory, the files `tasks.json` and `launch.json` tell VSCode how build the code and how to run it, respectively. (Note that `launch.json` references the build task defined in `tasks.json`.)

Transpiled JavaScript files and their source maps (which is needed when setting a breakpoint) end up in the `dist` directory. You shouldn't really have to deal with this directory.

## Runing code

After you've added whatever code you want to `main.ts` (or if you just want to test the initial Hello World solution), you can run the code by pressing F5. The code will be re-compiled before being run, so any changes you have will get incorporated automatically. The output will appear in the Debug Console within VSCode, which should open automatically. If you have any breakpoints in VSCode, these breakpoints will be hit. If you want to run code without hitting breakpoints, you can use CTRL + F5.

## Building code without running

While most of the time you will likely just want to build and run at the same time, there may be a point where you want to build without running (for example, to weed out build errors). To do this, press CTRL + SHIFT + B.
