# codelabs.cs.pdx.edu setup
---
`labs` contain individual codelabs
`tools` contain the site pages that collect individual codelabs together based on how they are tagged
---
```sudo apt update -y
sudo apt install golang npm make -y
npm install gulp-cli -g
go get github.com/googlecodelabs/tools/claat
cat << EOF >> .profile
if [ -d "$HOME/go/bin" ] ; then
    PATH="$HOME/go/bin:$PATH"
fi
EOF
git clone https://github.com/wu4f/codelabs_pdx.git
cd codelabs_pdx/tools/site/
npm install
```
