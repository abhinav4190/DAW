# Run Locally on MacOS ARM

```
# Download and build the source code
git clone --recursive https://github.com/abhinav4190/DAW.git
cd stargate/src
./macos/homebrew_deps.sh
python3 -m venv venv
. venv/bin/activate
pip3 install -r macos/requirements-m1.txt
pip3 install -e .
make macos_arm
python3 ./scripts/stargate

Now you will see the application will open.

Note that you may need to disable the Mac OS X firewall (if enabled) or
add rules, as it may block the Stargate UI and engine from communicating over
UDP sockets on localhost.  You will need the following rules:
```
stargate: 31909
stargate-engine: 31999
```



![Banner](assets/banner.png?raw=true "Banner")