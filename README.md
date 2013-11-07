# gitlab-dpkg
Debian-Folder to build GitLab DPKG-Package.

## Prepare Build-Folder

    git clone https://github.com/gitlabhq/gitlabhq gitlab_6.2.3

    cd gitlab_6.2.3 && git checkout v6.2.3

    git clone https://github.com/gitlabhq/gitlab-shell

    cd gitlab-shell && git checkout v1.7.6

    cd ../.. && tar -zcf gitlab_6.2.3.orig.tar.gz gitlab_6.2.3

    cd gitlab_6.2.3 && git clone https://github.com/1and1/gitlab-dpkg debian

    cd debian && git checkout squeeze-6-2-update

## Prepare Debian Squeeze

    apt-get install autoconf automake bundler debhelper libcurl4-openssl-dev libffi-dev libgdbm-dev libicu-dev libmagic-dev libmysqlclient-dev libncurses5-dev libpq-dev libreadline-dev libruby1.9.1 libssl-dev libxml2-dev libxslt1-dev libyaml-dev quilt ruby1.9.3 ruby1.9.1-dev zlib1g-dev

## Build Package:

    cd .. && dpkg-buildpackage
