A python project that uses origin files to manage a large music library.  All albums need to have origin files in the album folders with the metadata you want to use.  Then you run three sets of scripts.

The first phase is meant to get you all the metadata you need and prepare the files without altering them.  You can seed the files in this state. In the first phase you are checking to see if you have the origin files themselves, grabbing cover art, merging data from the files into the origin file and then running freezetag to preserve the metadata and files in case you want to reverse the next few steps.

The second phase is sorting the albums.  It standardizes the folder names (which is needed to assign disc numbers properly), looks for missing tags that would break later steps, looks for albums which have label/cat numbers but not for the specific edition, and then seperates out albums which are compilations, classical or DJ mixes so they can be tagged in different ways.

The third phase uses the meta data acquired in the first step to overwrite the VORBIS tags and assign genres and styles, it then renames the flac files to a template of your preference (ie. track number - track name) and finally moves the albums into a Artist/Album folders. 

The fourth phase is just adding them to your music app.

This is the order of the scripts that are run.

Phase 1: Collect
M:\music-util\origin-scripts\Missing-Origin\Missing-Origin.py
M:\music-util\origin-scripts\Origin-Cover\Origin-Cover.py
M:\music-util\origin-scripts\Origin-Combine-Genres\Origin-Combine-Genres.py
M:\music-util\origin-scripts\FreezeTag-Recursive\FreezeTag-Recursive.py

Phase 2: Sort
M:\music-util\origin-scripts\Standard-Folder\Standard-Folder.py
M:\music-util\origin-scripts\Find-Missing-Tags\Find-Missing-Tags.py
M:\music-util\origin-scripts\Origin-Find-Missing-Labels\Origin-Find-Missing-Labels.py
M:\music-util\origin-scripts\Sort-Origin\Sort-Origin.py

Phase 3: Tag & Rename
M:\music-util\origin-scripts\Origin-Write-Metadata\Origin-Write-Metadata.py
M:\music-util\origin-scripts\Origin-Write-Genres\Origin-Write-Genres.py
M:\music-util\origin-scripts\Rename-Flac-Files\Rename-Flac-Files.py
M:\music-util\origin-scripts\Sort-Rename\Sort-Rename-Music-Directory.py


Phase 4: 
add to music library