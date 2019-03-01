# Jupyter App Mac

## Disclaimer
I am not associated with Jupyter, and I don't own the logo, so if there's an issue with any of this repository existing, I apologize. Please let me know and I'll take it down. Thank you.

## What This Is
This is just a simple Mac app created with Automator that launches jupyter notebook when ran. If it is run with an iPython notebook (.ipynb), it'll launch jupyter notebook and open that notebook.

## Why
I was tired of opening Terminal, changing directories to the .ipynb file, typing `jupyter notebook`, and clicking on the notebook.

## Considerations
This may not work if you don't have jupyter notebook installed in `/usr/local/bin/`  
If you have it installed elsewhere, recreate it with Automator using your install location.

### How to Recreate
1. Open Automator
2. Add a "Run Shell Script" action
3. Make sure "as arguments" is selected for the passed input
4. Put `/usr/local/bin/jupyter notebook "$1"` as the script that runs
5. Save in your desired folder (I like /Applications so it shows up in the Launchpad)
6. Run it by itself or assign it as the default application for .ipynb files and open the .ipynb file
7. Enjoy the slight increase in efficiency

Another consideration is that it doesn't open an actual Terminal. This means you can't `ctl+c` and correctly shut down the notebook server. To quit the app (and stop the server), you have to stop the app from the menu bar by clicking on the spinning gear and then on the 'x'. This is probably bad practice, so make sure you save your notebook before quitting the app.


## Future Development
I'm sure it'd be great to upload source code and have it build for your system or something, but this is just a simple thing, so I'll let it be.

Created by Jonathan Osborne Contreras  TheJonWZ@Gmail.com