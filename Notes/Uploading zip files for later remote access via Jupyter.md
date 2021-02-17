**Disclaimer: this method requires you to continually purchase datapacks with each instance of fetching the file.**
**Unfortunately, this resulted in my GitLFS being disabled for a whole month. Avoid at all costs.**

Run the following commands in Git Bash to upload the `.zip` file using Git Bash and Git LFS:
```
git checkout -b master
git status
git remote set-url https://github.com/CeeThinwa/DeepLearning.AI-TensorFlow-Developer-Journey.git
git origin add https://github.com/CeeThinwa/DeepLearning.AI-TensorFlow-Developer-Journey.git
git remote -v
cd C://Users/CT/Documents/GitHub/DeepLearning.AI-TensorFlow-Developer-Journey
git lfs track "horse-or-human.zip"
git add horse-or-human.zip
git commit -m 'Added zip file of images'
git status
git push
```

Open the file hosted on GitHub in your Binder (an instance of Jupyter Hub) via your notebook using `wget` as follows:

```
!wget --no-check-certificate \
    https://github.com/CeeThinwa/DeepLearning.AI-TensorFlow-Developer-Journey/blob/master/horse-or-human.zip?raw=true \
    -O /tmp/horse-or-human.zip
```
