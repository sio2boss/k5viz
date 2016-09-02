k5viz
=====

k5viz is a simple application that can read in a [k5](https://github.com/sio2boss/k5-spec) file (coming soon) or JSON graph file and visualize the Deep Learning neural network for you.  Much of the code has been pulled from [mxnet](https://github.com/dmlc/mxnet) but no need to install it.

Example Usage
-------------

Grab the Inception v3 network that has been converted to mxnet, extract it, and visualize it.  Here we use [har](https://github.com/sio2boss/har) to do the download, extract, and remove the downloaded tar.gz file.

    # Grab k5viz (pip install coming soon)
    git clone https://github.com/sio2boss/k5viz.git && cd k5viz

    # Install har
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/sio2boss/har/master/tools/install.sh)"

    # Grab network
    har http://data.dmlc.ml/mxnet/models/imagenet/inception-v3.tar.gz

	# Grab dependencies
    sudo pip install graphviz docopt

    # Visualize
    python k5viz.py model/Inception-7-symbol.json
    
    
TODO
----
 - [x] Visualize without requiring mxnet
 - [ ] Read from k5
 - [ ] Enable pip install

License
-------
© Contributors, 2016. Licensed under an [Apache-2.0](https://github.com/sio2boss/k5viz/blob/master/LICENSE) license.
