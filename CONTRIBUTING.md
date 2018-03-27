# Let's Make a Voxel Engine
### A C# Voxel Framework

[Contributing](#contributing)
[Best Practices for Contributing](#best-practices-for-contributing)  
[File Formats](#file-formats)

## Contributing

If you would like to contribute to this project by adding/modifying the program code and/or various creative assets, please read the [Best Practices for Contributing](#best-practices-for-contributing) below and feel free to follow the standard GitHub workflow:

1. Fork the project.
2. Clone your fork to your local computer.
 * From the command line: `git clone https://github.com/<USERNAME>/UnityCraft.git`
3. Change into your new project folder.
 * From the command line: `cd UnityCraft`
4. [optional] Add the upstream repository to your list of remotes.
 * From the command line: `git remote add upstream https://github.com/ArclightTW/UnityCraft.git`
5. Create a branch for your new feature.
 * From the command line: `git checkout -b <BRANCH-NAME>`
6. Make your changes.
 * Avoid making changes to more files than necessary for your feature (i.e. refrain from combining your "real" Pull Request with incidental bug fixes and/or code tidy-up).  This will simplify the merging process and make your changes clearer.
 * Avoid making changes to Unity-specific files, like the scene and project settings, unless absolutely necessary.  Changes here are likely to cause difficult to merge conflicts.  Work within the code structure as much as possible.  Changing prefabs should generally be safe to do so, but make any changes in a new scene that is deleted prior to your commit, not within any of the existing project scenes.
7. Commit your changes.
 * From the command line: `git add <CHANGED-FILE>`
 * Repeat for as many files as necessary
 * From the command line: `git commit -m "<DESCRIPTIVE COMMIT MESSAGE>"`
8. While you were working on your Pull Request, another Pull Request might have been merged that breaks your code and/or vice versa.  This could be a _merge conflict_ but may also be conflicting game logic or code.  Before you test, merge with the master project.
 * From the command line: `git fetch upstream`
 * From the command line: `git merge upstream/master`
9. Test.  Start the game and do something related to your feature/fix.
10. Push the branch, uploading it to GitHub.
 * From the command line: `git push origin <BRANCH-NAME>`
11. Make a Pull Request from your branch on GitHub.
 * Include screenshots and/or videos demonstrating your change, if applicable.
12. The Pull Request will either be accepted or rejected by the project manager; if rejected, make any relevant changes to your Pull Request so it can be accepted without error.

## Best Practices for Contributing

* Before you start coding, open an issue so that the community can discuss your change to ensure it is in line with the goals of the project and is not already being worked on.  This allows for discussion and fine tuning of your feature and results in a more succint and focused addition:
	* If you are fixing a minor glitch or bug, you may make a Pull Request without opening an issue.
	* If you are adding a large feature, create an issue prefixed with "[Discussion]" and be sure to take community feedback and get general approval before making your changes and submitting a Pull Request.
* Pull Requests represent final code.  Please ensure they are:
	* Well tested by the author.  It is the author's job to ensure their code works as expected.
	* Be free of unnecessary logging.  Log calls should only be present when there is an actual error or to warn of an unimplemented feature.  "Debug" log calls should be removed entirely.
	If your code is untested, log heavy or incomplete and a Pull Request has been created, prefix it with "[WIP]" so others know that it is still being tested and should not be considered for merging yet.
* Small changes are preferable over larger ones.  The larger a change, the more likely it is to conflict with the project and, thus, be rejected.  If your addition is large, be sure to extensively discuss it in an "issue" prior to beginning a change or submitting a Pull Request.
* Try to keep your Pull Request focused to the specific feature/fix you are working on; changes to unnecessary code complicates the merging process, as there may be small changes that make your Pull Request unacceptable whilst the majority of the code is ready to merge.
* Limit any changes to code definitions (variables, functions, properties and classes/structs/interfaces):
	* A restructure/overhaul is defined as the focus being on the entire system rather than a small module so almost every one of these 'cautions' are void in that case.
	* Any changes to functions should be limited; you should try to work 'within' the current system.  This does not apply to restructures as this is mainly due to a lack of ability of the current system to achieve a goal.
	* Adding new public variables should always be a cautionary procedure; only do so if a private variable is being exposed for modding purposes or public variables are being removed due to a lack of need.  As above, this does not apply to restructures/overhauls or new systems.
	* Do not remove any classes/structs/interfaces unless your Pull Request is specifically a restructure/overhaul.
* Document your changes in your Pull Request.  If you add a feature that you expect others to use, explain exactly how future code should interact with your additions.
* Avoid making changes to more files than necessary for your feature.
* Avoid making changes to Unity-specific files.
* Include screenshots and/or videos demonstrating your change, if applicable.

## File Formats

### Images
Images should be submitted only in PNG format.  Any original files, such as Photoshop/GIMP/Paint.net files, are not to be committed to the repository, as they take up unnecessary storage.  Hosting the originals in a public location, such as a public Dropbox or Google Drive folder, however, is appreciated (but not required).

### Audio
Audio files should be submitted only in the open-source friendly OGG audio format, as opposed to MP3 or uncompressed WAV files.  Small sound effects that are played frequently should be set to "Decompress on Load" in Unity's inspector, whereas larger sounds (such as songs) should not be.  Hosting the originals in a public location, such as a public Dropbox or Google Drive folder, is appreciated (but not required).
