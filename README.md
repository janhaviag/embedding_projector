# embedding_projector

# Running tensorboard embedding projector locally

Install Bazel in Linux - this installs the most recent version of Bazel (note it is not compatible with the example in https://github.com/tensorflow/tensorboard-plugin-example)
```shell
echo "deb [arch=amd64] https://storage.googleapis.com/bazel-apt stable jdk1.8" | sudo tee /etc/apt/sources.list.d/bazel.list
curl https://bazel.build/bazel-release.pub.gpg | sudo apt-key add -

# install and update
sudo apt-get update && sudo apt-get install bazel
```

Clone/Fork tensorboard repo
```shell
git clone git@github.com:tensorflow/tensorboard.git
```

Run the projector
```shell
bazel run tensorboard/plugins/projector/vz_projector:devserver
