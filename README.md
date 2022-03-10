# codelabs.cs.pdx.edu setup
---
`labs` contain individual codelabs
`tools` contain the site pages that collect individual codelabs together based on how they are tagged
---
```
# Install claat in $HOME/go/bin
#  https://github.com/googlecodelabs/tools/releases/latest
#  https://github.com/googlecodelabs/tools/releases/tag/v2.2.4
sudo apt update -y
sudo apt install npm make -y
sudo npm install gulp-cli -g
cat << EOF >> .profile
if [ -d "\$HOME/go/bin" ] ; then
    PATH="\$HOME/go/bin:\$PATH"
fi
EOF
source .profile
git clone https://github.com/wu4f/codelabs_pdx.git
cd codelabs_pdx/tools/site/
npm install
```
