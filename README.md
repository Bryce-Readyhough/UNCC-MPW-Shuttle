# Analog Spiking Neuron Circuit - Caravel Submission

This is the Google/EFabless/Skywater Caravel submission of an [Analog Spiking Neuron Circuit.](https://ieeexplore.ieee.org/document/9184447) The submission also includes a SONOS transistor array. 

TODO: Add block diagram

[comment]: <> (<p align=”center”>)
[comment]: <> (<img src="/doc/ciic_harness.png" width="75%" height="75%"> )
[comment]: <> (</p>)

# Installation and Usage
To setup and install the repo for development:</br>
<ol>
	<li>Install prerequisite tools:</li>
	<ol>
		<li>Install [Magic VLSI Layout Tool](http://opencircuitdesign.com/magic/)</li>
			<ol>
				<li>Note: As of the writing of this document the tool must be installed from sourcecode. The packaged version is not up to date for use with this repo.</li>
			</ol>
		<li>Install [KLayout VLSI Layout Tool](https://www.klayout.de/build.html)</li>
		<li>Install [SkywaterPDK](https://github.com/google/skywater-pdk) and [OpenPDK](https://github.com/RTimothyEdwards/open_pdks):</li>
			<ol>
				<li>Install Skywater PDK</li>
				<code>
					export PDK_ROOT=<Absolute path where PDKs will be installed>
					cd $PDK_ROOT
					git clone https://github.com/google/skywater-pdk
					cd skywater-pdk
					git submodule init libraries/sky130_fd_io/latest
					git submodule init libraries/sky130_fd_pr/latest
					git submodule init libraries/sky130_fd_sc_hd/latest
					git submodule init libraries/sky130_fd_sc_hdll/latest
					git submodule init libraries/sky130_fd_sc_hs/latest
					git submodule init libraries/sky130_fd_sc_ms/latest
					git submodule init libraries/sky130_fd_sc_ls/latest
					git submodule init libraries/sky130_fd_sc_lp/latest
					git submodule init libraries/sky130_fd_sc_hvl/latest
					git submodule update
					make timing
				</code>
				<li>Install OpenPDKs</li>
				<code>	
					git clone https://github.com/RTimothyEdwards/open_pdks.git
					cd open_pdks
					./configure --with-sky130-source=$PDK_ROOT/skywater-pdk/libraries --with-sky130-local-path=$PDK_ROOT
					cd sky130
					make
					make install-local
				</code>
			</ol>
		</li> Test Line Item </li>
	</ol>
</ol>
 
TODO: Finish Install instructions
