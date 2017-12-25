<p align="center"><img src="https://raw.githubusercontent.com/anfederico/cryptoview/master/media/logo.png" width="400px"><p>
    
<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Python](https://img.shields.io/badge/python-v3.6-blue.svg)
![Dependencies](https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg)
[![GitHub Issues](https://img.shields.io/github/issues/anfederico/cryptoview.svg)](https://github.com/anfederico/cryptoview/issues)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

<p align="center"><img src="https://raw.githubusercontent.com/anfederico/cryptoview/master/media/example.png" width="70%"><p>

## Briefly
Cryptoview can be run locally however it is written to be forked and deployed on a free Heroku account. The only thing you need to do is setup a free online database through mlab, edit a settings file, and deploy straight from Github. I've tried to make these steps as easy as possible.

## Setting up the database
- Make an account at https://mlab.com
- Create a new deployment in sandbox mode
- Add a database user to your deployment
- Keep the site up for the next step

## Fork and fill out the settings file
```
/cryptoview
└── /scripts
    └── settings.py
```

## Run it local or on Heroku 
To run it locally, just start up the web application and updater files. The updaters script is what is tracking the account equity and updating the mongo database.
```
python app.py
python updaters.py
```
The reason it runs separately is to keep web hosting free, if you decide to host it on Heroku. By handling the background tasks locally, you can run app.py in sandbox mode on Heroku and handle the updaters file on your local computer. Since mlab is an online database, both Heroku and your local computer can communicate through it. I prefer this method because I can access my portfolio from anywhere online without paying for extra Heroku dynos. All you have to do is fork the repository, deploy from it through Heroku, and then once it is deployed, run updaters.py on your local computer.

## Contributions
Please [create an issue](https://github.com/anfederico/cryptoview/issues/new) for any ideas/comments/features you'd like to see or implement yourself!

## Tips
![BTC](https://img.shields.io/badge/BTC-14hBuV5SgfeMQN5ejV7S3Gocaajbg5B5Rx-yellow.svg)<br>
![ETH](https://img.shields.io/badge/ETH-0x72D7358F875C55441BbEF3b3984cbf3AE5F34F2a-brightgreen.svg)<br>
![LTC](https://img.shields.io/badge/LTC-LhEx3SGL6gmBPAteSwZdwKaNDTvU3mGQDz-lightgrey.svg)
