### Making ionizing flux - density plots using outputs from python and cloudy 
This notebook shows you how to make ionizing flux v density plots of the kind in Matthews et al. 2020 (M20), where we compare outputs from a disc wind model to those from cloudy. The ionizing photon flux $\phi_H$ is related to the ionization parameter $U$ by 
$$\phi_H = U c n_H $$
(see equations in sec 2 of M20). 

The basic procedure here is:
* read line emissivities and so on from cloudy grid, stored in data/cloudy_lines.dat
* read outputs from py_wind; ideally use your own, but I've example outputs in data/
* plot the result

**Prerequisites:**
To create the outputs from py_wind, compile py_wind with the same version of the code you used to run the code, and then run 

    py_wind < py_wind_cmds.txt
    
where the file py_wind_cmds.txt is a file included in the repository and should generate the right files. 

This code requires ```numpy```, ```matplotlib```, and also uses the routine ```py_read_output```, which means you should add ```$PYTHON/py_progs/``` to your ```$PYTHONPATH``` environment variable.
