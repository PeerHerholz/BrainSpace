# Your version: 0.6.0 Latest version: 0.6.0
# Generated by Neurodocker version 0.6.0
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
# Timestamp: 2020-02-19 18:31:33 UTC
=======
# Timestamp: 2020-02-11 20:25:28 UTC
>>>>>>> include container info
=======
# Timestamp: 2020-02-11 20:58:21 UTC
>>>>>>> update container informatio
=======
# Timestamp: 2020-02-11 20:25:28 UTC
>>>>>>> include container info
=======
# Timestamp: 2020-02-11 20:58:21 UTC
>>>>>>> update container informatio
# 
# Thank you for using Neurodocker. If you discover any issues
# or ways to improve this software, please submit an issue or
# pull request on our GitHub repository:
# 
#     https://github.com/kaczmarj/neurodocker

Bootstrap: docker
From: ubuntu:latest

%post
export ND_ENTRYPOINT="/neurodocker/startup.sh"
apt-get update -qq
apt-get install -y -q --no-install-recommends \
    apt-utils \
    bzip2 \
    ca-certificates \
    curl \
    locales \
    unzip
apt-get clean
rm -rf /var/lib/apt/lists/*
sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen
dpkg-reconfigure --frontend=noninteractive locales
update-locale LANG="en_US.UTF-8"
chmod 777 /opt && chmod a+s /opt
mkdir -p /neurodocker
if [ ! -f "$ND_ENTRYPOINT" ]; then
  echo '#!/usr/bin/env bash' >> "$ND_ENTRYPOINT"
  echo 'set -e' >> "$ND_ENTRYPOINT"
  echo 'export USER="${USER:=`whoami`}"' >> "$ND_ENTRYPOINT"
  echo 'if [ -n "$1" ]; then "$@"; else /usr/bin/env bash; fi' >> "$ND_ENTRYPOINT";
fi
chmod -R 777 /neurodocker && chmod a+s /neurodocker

bash -c 'apt-get update'

apt-get update -qq
apt-get install -y -q --no-install-recommends \
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
    git \
=======
>>>>>>> include container info
=======
    git \
>>>>>>> update container informatio
=======
>>>>>>> include container info
=======
    git \
>>>>>>> update container informatio
    libsm6 \
    libxext6 \
    libgl1-mesa-dev \
    libvtk6.3 \
    xvfb
apt-get clean
rm -rf /var/lib/apt/lists/*

su - root

<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
bash -c 'curl https://raw.githubusercontent.com/PeerHerholz/BrainSpace/initial_draft_virtualization/requirements.txt > requirements.txt && chmod 777 requirements.txt'
=======
bash -c 'curl https://raw.githubusercontent.com/PeerHerholz/BrainSpace/master/requirements.txt > requirements.txt && chmod 777 requirements.txt'
>>>>>>> include container info
=======
bash -c 'curl https://raw.githubusercontent.com/PeerHerholz/BrainSpace/master/requirements.txt > requirements.txt && chmod 777 requirements.txt'
>>>>>>> include container info

test "$(getent passwd brainspace)" || useradd --no-user-group --create-home --shell /bin/bash brainspace
su - brainspace

export PATH="/opt/miniconda-latest/bin:$PATH"
echo "Downloading Miniconda installer ..."
conda_installer="/tmp/miniconda.sh"
curl -fsSL --retry 5 -o "$conda_installer" https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash "$conda_installer" -b -p /opt/miniconda-latest
rm -f "$conda_installer"
conda update -yq -nbase conda
conda config --system --prepend channels conda-forge
conda config --system --set auto_update_conda false
conda config --system --set show_channel_urls true
sync && conda clean --all && sync
conda create -y -q --name brainspace
conda install -y -q --name brainspace \
    "python=3.7" \
    "panel" \
    "pyqt" \
    "pyvista" \
    "notebook" \
    "ipython"
sync && conda clean --all && sync
bash -c "source activate brainspace
  pip install --no-cache-dir  \
      "-r" \
      "requirements.txt" \
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
      "git+https://github.com/PeerHerholz/BrainSpace.git@notebook_binder_support" \
=======
      "brainspace" \
>>>>>>> include container info
=======
      "git+https://github.com/PeerHerholz/BrainSpace.git@notebook_binder_support" \
>>>>>>> update container informatio
=======
      "brainspace" \
>>>>>>> include container info
=======
      "git+https://github.com/PeerHerholz/BrainSpace.git@notebook_binder_support" \
>>>>>>> update container informatio
      "xvfbwrapper" \
      "ipywidgets" \
      "ipyevents" \
      "jupytext" \
      "seaborn""
rm -rf ~/.cache/pip/*
sync
sed -i '$isource activate brainspace' $ND_ENTRYPOINT


mkdir -p ~/.jupyter && echo c.NotebookApp.ip = \"0.0.0.0\" > ~/.jupyter/jupyter_notebook_config.py

cd /opt/miniconda-latest/envs/brainspace/lib/python3.7/site-packages/brainspace/examples

sed -i '$ijupytext --set-formats ipynb,py *.py && rm *.ipynb' $ND_ENTRYPOINT

echo '{
\n  "pkg_manager": "apt",
\n  "instructions": [
\n    [
\n      "base",
\n      "ubuntu:latest"
\n    ],
\n    [
\n      "_header",
\n      {
\n        "version": "generic",
\n        "method": "custom"
\n      }
\n    ],
\n    [
\n      "run_bash",
\n      "apt-get update"
\n    ],
\n    [
\n      "install",
\n      [
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
\n        "git",
=======
>>>>>>> include container info
=======
\n        "git",
>>>>>>> update container informatio
=======
>>>>>>> include container info
=======
\n        "git",
>>>>>>> update container informatio
\n        "libsm6",
\n        "libxext6",
\n        "libgl1-mesa-dev",
\n        "libvtk6.3",
\n        "xvfb"
\n      ]
\n    ],
\n    [
\n      "user",
\n      "root"
\n    ],
\n    [
\n      "run_bash",
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
\n      "curl https://raw.githubusercontent.com/PeerHerholz/BrainSpace/initial_draft_virtualization/requirements.txt > requirements.txt && chmod 777 requirements.txt"
=======
\n      "curl https://raw.githubusercontent.com/PeerHerholz/BrainSpace/master/requirements.txt > requirements.txt && chmod 777 requirements.txt"
>>>>>>> include container info
=======
\n      "curl https://raw.githubusercontent.com/PeerHerholz/BrainSpace/master/requirements.txt > requirements.txt && chmod 777 requirements.txt"
>>>>>>> include container info
\n    ],
\n    [
\n      "user",
\n      "brainspace"
\n    ],
\n    [
\n      "miniconda",
\n      {
\n        "conda_install": [
\n          "python=3.7",
\n          "panel",
\n          "pyqt",
\n          "pyvista",
\n          "notebook",
\n          "ipython"
\n        ],
\n        "pip_install": [
\n          "-r",
\n          "requirements.txt",
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
<<<<<<< refs/remotes/origin/initial_draft_virtualization
\n          "git+https://github.com/PeerHerholz/BrainSpace.git@notebook_binder_support",
=======
\n          "brainspace",
>>>>>>> include container info
=======
\n          "git+https://github.com/PeerHerholz/BrainSpace.git@notebook_binder_support",
>>>>>>> update container informatio
=======
\n          "brainspace",
>>>>>>> include container info
=======
\n          "git+https://github.com/PeerHerholz/BrainSpace.git@notebook_binder_support",
>>>>>>> update container informatio
\n          "xvfbwrapper",
\n          "ipywidgets",
\n          "ipyevents",
\n          "jupytext",
\n          "seaborn"
\n        ],
\n        "create_env": "brainspace",
\n        "activate": true
\n      }
\n    ],
\n    [
\n      "run",
\n      "mkdir -p ~/.jupyter && echo c.NotebookApp.ip = \\\"0.0.0.0\\\" > ~/.jupyter/jupyter_notebook_config.py"
\n    ],
\n    [
\n      "entrypoint",
\n      "/neurodocker/startup.sh"
\n    ],
\n    [
\n      "workdir",
\n      "/opt/miniconda-latest/envs/brainspace/lib/python3.7/site-packages/brainspace/examples"
\n    ],
\n    [
\n      "add_to_entrypoint",
\n      "jupytext --set-formats ipynb,py *.py && rm *.ipynb"
\n    ]
\n  ]
\n}' > /neurodocker/neurodocker_specs.json

%environment
export LANG="en_US.UTF-8"
export LC_ALL="en_US.UTF-8"
export ND_ENTRYPOINT="/neurodocker/startup.sh"
export CONDA_DIR="/opt/miniconda-latest"
export PATH="/opt/miniconda-latest/bin:$PATH"

%runscript
/neurodocker/startup.sh
