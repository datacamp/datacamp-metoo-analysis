# How the #MeToo Movement Spread on Twitter
What can data science tell us about tweets with the #MeToo hashtag? This repository contains the code for the analysis [here](https://www.datacamp.com/community/blog/metoo-twitter-analysis).

Below I include how to get set up with the correct Python packages. After this, I provide instructions on how to use these notebooks to reproduce my analysis using the Twitter API. I encourage questions, feedback and pull requests.

## Getting set up computationally

### 1. Clone the repository

To get set up for this live coding session, clone this repository. You can do so by executing the following in your terminal:

```
git clone https://github.com/datacamp/datacamp-metoo-analysis
```

Alternatively, you can download the zip file of the repository at the top of the main page of the repository. If you prefer not to use git or don't have experience with it, this a good option.

### 2. Download Anaconda (if you haven't already)

If you do not already have the [Anaconda distribution](https://www.anaconda.com/download/) of Python 3, go get it (n.b., you can also do this w/out Anaconda using `pip` to install the required packages, however Anaconda is great for Data Science and I encourage you to use it).

### 3. Create your conda environment for this session

Navigate to the relevant directory `datacamp-metoo-analysis` and install required packages in a new conda environment:

```
conda env create -f environment.yml
```

This will create a new environment called ds-twitter. To activate the environment on OSX/Linux, execute

```
source activate ds-twitter
```
On Windows, execute

```
activate ds-twitter
```

## Getting the tweets for the analysis

To protect Twitter users who may have deleted their tweets, Twitter does not allow my to share the actual tweets that I used for the analysis. I can, however, share the tweet IDs. I have done so in the `/data` subdirectory and in the `get_tweets.ipynb` notebook I have provided the code that will allow you to pull all the tweets that still exist in from the Twitter API.

To do so, you will need to

* get set up w/ the Twitter API (see below).
* Store your Twitter API credentials in a `config.yml` file (template in this repository).

After you have the tweets, you can generate the word clouds using `word_clouds.ipynb`. You can also reproduce my analysis using `MeToo_analysis_w_code.ipynb`.

### Accessing the Twitter API

I have taken this verbatim from [Adil Moujahid's post here](http://adilmoujahid.com/posts/2014/07/twitter-analytics/) as he said it so well.

In order to access Twitter Streaming API, we need to get 4 pieces of information from Twitter: API key, API secret, Access token and Access token secret. Follow the steps below to get all 4 elements:

* Create a twitter account if you do not already have one.
* Go to https://apps.twitter.com/ and log in with your twitter credentials.
* Click "Create New App"
* Fill out the form, agree to the terms, and click "Create your Twitter application"
* In the next page, click on "API keys" tab, and copy your "API key" and "API secret".
* Scroll down and click "Create my access token", and copy your "Access token" and "Access token secret".

### Code
The code in this repository is released under the [MIT license](LICENSE). Read more at the [Open Source Initiative](https://opensource.org/licenses/MIT). All text remains the Intellectual Property of DataCamp. If you wish to reuse, adapt or remix, get in touch with me at hugo at datacamp com to request permission.
