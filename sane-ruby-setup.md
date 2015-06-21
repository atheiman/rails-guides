# Sane and Simple Ruby Setup with `chruby` and `ruby-install`

1. [Install `ruby-install`](https://github.com/postmodern/ruby-install#install)

```
wget -O ruby-install-0.5.0.tar.gz https://github.com/postmodern/ruby-install/archive/v0.5.0.tar.gz
tar -xzvf ruby-install-0.5.0.tar.gz
cd ruby-install-0.5.0/
sudo make install
```

1. [Install `chruby`](https://github.com/postmodern/chruby#install)

```
wget -O chruby-0.3.9.tar.gz https://github.com/postmodern/chruby/archive/v0.3.9.tar.gz
tar -xzvf chruby-0.3.9.tar.gz
cd chruby-0.3.9/
sudo ./scripts/setup.sh
```

1. Test setup so far

```
# show available rubies
ruby-install
# install a ruby to ~/.rubies
ruby-install 2.1.3
# activate chruby
source /usr/local/share/chruby/chruby.sh
# change to installed ruby
chruby 2.1.3
# check the ruby version
ruby --version
# show the location of the ruby binary
which ruby
# show your gem enivronment info
gem env
```

1. Configure `chruby`

# activate chruby when starting shell
echo "source /usr/local/share/chruby/chruby.sh" >> ~/.bashrc
# set a default ruby
echo "chruby 2.1.3" >> ~/.bashrc
