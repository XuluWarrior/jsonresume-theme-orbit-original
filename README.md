# JSON Resume Orbit Original Theme 
This is a theme for [JSON Resume](http://jsonresume.org/) based on [Orbit design](https://github.com/xriley/Orbit-Theme) by [xriley](https://github.com/xriley).
The theme uses the same headings as [Orbit-Theme](https://github.com/xriley/Orbit-Theme) and doesn't support all the sections in the JSON Resume [schema](https://jsonresume.org/schema/).
For a more complete template see [jsonresume-theme-orbit](https://github.com/XuluWarrior/jsonresume-theme-orbit).

[![Example resume](https://xuluwarrior.github.io/jsonresume-theme-orbit-original/resume.png)](https://xuluwarrior.github.io/jsonresume-theme-orbit-original/resume.html)

## Differences
There is one slight difference between the version of this theme on npm and the original design.  The sidebar is wider to fit the longer profile urls used in the example resume.json from [jsonresume.org](https://jsonresume.org/).
To use the original width (240px) run the template locally.  See **Editing template** for instructions.
## Getting started

### Install the command line

Install [resume-cli](https://github.com/jsonresume/resume-cli) to render your resume.

```
sudo npm install -g resume-cli
```

### Serve theme
```
resume serve --theme orbit-original --resume <path_to_resume.json>
```

You should now see this message:

```
Preview: http://localhost:4000
Press ctrl-c to stop
```

The resume should open in a new tab in your default browser

## Editing template
### Get source from GitHub
```
git clone https://github.com/XuluWarrior/jsonresume-theme-orbit-original.git
cd jsonresume-theme-orbit-original
```

### Serve theme
```
resume serve
```
This will use the local version of the theme to render the resume.json
If there is a local copy of resume.json this will be used.  Otherwise, it will use the default resume.json from [jsonresume.org](https://jsonresume.org/)

### Change color scheme
This theme comes with 6 color schemes.  To change to an alternative run the build:styles script where 2 >= i <= 6
```
npm run build:styles:<i>
```

To revert to the default theme
```
npm run build:styles
```

### Change width of sidebar
If profile details are too wide for the sidebar (as with the example resume.json from [jsonresume.org](https://jsonresume.org/)) then edit **less/default/base.less** and change @sidebar-width
e.g.
```
@sidebar-width: 300px;
```
Rebuild styles.css with the appropriate build:styles command.
e.g.
```
npm run build:styles
```

## License
Template design is available under [Creative Commons Attribution 3.0 License](http://creativecommons.org/licenses/by/3.0/) attributed to [xriley](https://github.com/xriley)

Source code for generating resume is available under [the MIT license](http://mths.be/mit).
