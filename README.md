# sprout-wrap

This project uses [soloist](https://github.com/mkocher/soloist) and [librarian-chef](https://github.com/applicationsonline/librarian-chef)
to run a subset of the recipes in sprout's cookbooks.

This fork is very similar to the [pivotal-labs](https://github.com/pivotal-sprout/sprout-wrap) version except that we've decided to stick with RVM instead of rbenv for now.

Finally, if you've never used Chef before - we highly recommend you buy &amp; watch [this excellent 17 minute screencast](http://railscasts.com/episodes/339-chef-solo-basics) by Ryan Bates. 

## Installation under Mavericks (OS X 10.9)

### 1. Install Command Line Tools
  
    xcode-select --install

If you receive a message about the update server being unavailable and are on Mavericks, then you already have the command line tools.

### 2. Clone this project

    git clone https://github.com/al-jazeera-america/sprout-wrap.git
    cd sprout-wrap

### 3. Install soloist & and other required gems

    sudo gem install bundler
    sudo bundle

If you receive errors like this:

    clang: error: unknown argument: '-multiply_definedsuppress'

then try downgrading those errors like this:

    sudo ARCHFLAGS=-Wno-error=unused-command-line-argument-hard-error-in-future bundle

### 4. Run soloist

[You may want to modify your Energy Saver preferences (**System Preferences &rarr; Energy Saver &rarr; Computer Sleep &rarr; 3hrs**); depending on your network connection, soloist can take from 10 minutes to 2 hours to complete.]

    sudo bundle exec soloist

### If it failes and you need to re-start it, if RVM is already running:

    rvm use system
    
to use the system ruby.

## Roadmap

See Pivotal Tracker: https://www.pivotaltracker.com/s/projects/884116

## Discussion List

  Join [sprout-users@googlegroups.com](https://groups.google.com/forum/#!forum/sprout-users) if you use Sprout.

## References

* Slides from @hiremaga's [lightning talk on Sprout](http://sprout-talk.cfapps.io/) at Pivotal Labs in June 2013
* [Railscast on chef-solo](http://railscasts.com/episodes/339-chef-solo-basics) by Ryan Bates (PAID)
