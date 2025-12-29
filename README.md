First, make sure the machine you are working on has the correct github sshkey:
ssh-keygen
cd .ssh
ls
less id_rsa.pub
then paste into this file the github sshkey for your github account

Then using the github website make a new repository/project under github and land on the Quick setup with SSH instructions. 

On the local machine make a new directory foobar/ and cd to it.

git clone git@github.com:lizmarai/cs426web.git  (or whatever the pathway listed under Quick setup says under ssh).

cp -R all files to foobar ( cp -R ../Downloads/cs426_webpage-main/* cs426/)

cd cs426

cp -R _site docs

git add -f *





This is the source code for Prof. Jakob Eriksson's personal webpage, viewable at http://www.cs.uic.edu/~jakob. 
Feel free to fork this repo to make your own UIC-themed webpage. 

To use it, first install node. On a mac, that would be 
`brew install node`. On linux, `apt-get install nodejs npm`. 

Then install the static site generator 11ty and the CSS framework tailwind. 
`npm install -D @11ty/eleventy tailwindcss@latest`

To use this as a template, start by updatin the settings in `_data/defaults.json' to reflect your name, title and a suitable portrait. Delete the contents of 'photos/' and add some of your own. Use landscape oriented photos of high resolution, and with your face fairly prominent and centered. Then, simply edit `home.md`, `projects.md` and `news.md` with your own content, and you're good to go.

To try it out, run `npm start` in the main folder, and open your website in a browser using the URL `localhost:8080`. 
The `Makefile` contains a handy target for uploading your site to your Computer Science department `WWW` folder. Works for me, but your YMMV as that's a pretty outdated system.
