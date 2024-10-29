# DITA Topic Model - Microsoft Office Suite (draft)

This repo contains a DITA topic model (TM) related to Microsoft Office Suite.

## Authors

- Jordan Matheney
- Beth Morris

## Folders &amp; Files

- `.github`: Contains configuration files for "Github Actions".
- `assets`: Contains all assets used within the TM.
- `concepts`: Contains all concept topics.
- `references`: Contains all reference topics.
- `tasks`: Contains all task topics.
- `shared`: Contains all topic files that are shared across multiple maps.
- `out`: Contains all output folders.
- `themes`: Contains `.yaml` style configuration files.
- **Skeleton files**: All topic folders contain a single "skeleton" topic file for you to copy, whenever you need to quickly create a new file.
- `.keep` **files**: Ignore these files. They ensure that any empty folders are tracked by git. 
- `.gitignore`: This file tells git which files to ignore in the repo. You can leave this one be.

## Filenaming Conventions

- Task Topics: `t_verb_verbobject.dita`
- Concept Topics: `c_nounphrase.dita`
- Reference Topics: It varies, but something akin to `r_types_of_nounphrase.dita`
- Dita Maps: `_modelname.ditamap`

## Building Outputs with Github Actions

This repo uses Github Actions to create outputs. Refer to the following for details: 

- [.github/workflows/dita-ot-build-actions.yaml](.github/workflows/dita-ot-build-actions.yaml)
- [DITA User Docs - Using Github Actions](https://www.dita-ot.org/dev/topics/using-github-actions)
- [DITA Example YAML files](https://github.com/dita-ot/docs/blob/develop/samples/github-actions/build-using-a-project-file.yaml)

## Building Outputs Manually with the Command Line

See the DITA-OT user guide about how to generate output: [https://www.dita-ot.org/dev/topics/build-using-dita-command](https://www.dita-ot.org/dev/topics/build-using-dita-command)

### Sample DITA Commands

#### Help

To see all of the commands and parameters, use the following command:

```
dita --help
```

#### DITA options and arguments

```
-f == dita output format
-i == dita input map file
-o == dita output directory
-D&lt;property&gt;=&lt;value&gt; == add custom args
    with particular values to dita transformation
-filter &lt;file&gt; == filter and flagging file
```

#### Create an HTML5 site

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```

#### Create an HTML5 site with a custom CSS file

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
  -Dargs.cssroot='url/to/your/assets/folder' \
  -Dargs.css='${cssroot}/your-custom-css-file.css' \
  -Dargs.csspath='css' \
  -Dargs.copycss='yes'
```

#### Create a PDF

```
dita -f pdf -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```
## Project Maps
### User Scenario 1
IT trainers who will be teaching this content to employees.

These trainers want to give better presentations but may be limited on time to do in person practice with a peer. 

Trainers are comfortable with technology and presentation software as well as the software they are educating others on.

This class is open for people to sign up to learn more information on the topic

Experience: Intermediate computer user and PowerPoint user

Limitations: Need basic knowledge of how to build slideshows in PowerPoint

Willingness to practice their content and receive feedback to improve their teaching and presentation skills. 

Environment: In an office setting (at home or at work) with little distractions 

Time to deliver the entire presentation for feedback

#### Map


### User Scenario 2
Students enrolled in a public speaking course.

They will use this software during the semester to learn how to better their presentation skills. They will apply their rehershal notes to their presentations during a live, online session during the semester. 

Students are comfortable with technology and the presentation slides software software. 

This is a class open for people to enroll to learn more information on the topic and use for a college credit. 

Experience: Beginner computer user and PowerPoint software user.

Limitations: Need basic knowledge of how to permit access of their computer microphone and camera.

Need to understand how to giveTeams permission to share screens in their computer settings.

Willingness to practice using the PowerPoint software.

#### Map

