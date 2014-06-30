# gitlab-dpkg
Debian-Folder to build GitLab DPKG-Package.

## Prepare Build-Folder

    git clone https://github.com/gitlabhq/gitlabhq gitlab_7.0.0

    cd gitlab_7.0.0 && git checkout v7.0.0

    git clone https://github.com/gitlabhq/gitlab-shell

    cd gitlab-shell && git checkout v1.9.6

    cd ../.. && tar -zcf gitlab_7.0.0.orig.tar.gz gitlab_7.0.0

    cd gitlab_7.0.0 && git clone https://github.com/1and1/gitlab-dpkg debian

    cd debian && git checkout wheezy-7-0-stable

## Prepare Debian Wheezy

    apt-get install autoconf automake bundler debhelper libcurl4-openssl-dev libffi-dev libgdbm-dev libicu-dev libmagic-dev libmysqlclient-dev libncurses5-dev libpq-dev libreadline-dev libruby1.9.1 libssl-dev libxml2-dev libxslt1-dev libyaml-dev quilt ruby1.9.3 ruby1.9.1-dev zlib1g-dev

## Build Package:

    cd .. && dpkg-buildpackage
