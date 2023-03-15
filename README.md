# Win2019STIG

Tested on Ubuntu 81.04

```
cd microsoft-windows-server-2019-stig-baseline/
cd test/cookbooks/Win2019STIG/
wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install vagrant
CHEF_LICENSE: accept-silent
export CHEF_LICENSE=accept-silent
export KITCHEN_YAML=kitchen.vagrant.yml
apt-get install jq
ruby -v
echo "gem: --no-ri --no-rdoc" >> ~/.gemrc
gem install bundler
bundle config path vendor/bundle
bundle install
wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] http://download.virtualbox.org/virtualbox/debian $(lsb_release -cs) contrib"
apt-get install software-properties-common
sudo apt update && sudo apt install vagrant
apt-get install virtualbox-6.1
bundle exec kitchen create
```
