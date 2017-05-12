
***********************************************************************************

In this directory, you will find the NFsim models that correspond to the four types of
kinetic Tile Assembly Model (kTAM) implementations: 
- kTAM_Classic_sierpinski_slot.bngl - the classical kTAM model (denoted as model S1 in the manuscript)
- sierpinski_site.bngl - the model where tiles interact based on edge-to-edge interaction (denoted as model S2 in the manuscript)
- sierpinski_slot_matching_glues.bngl - the model derived from S1 but where an initial binding to the assembly can be done ONLY if at least one matching glue exists (denoted as model S3 in the manuscript)
- sierpinski_site_matching_glues.bngl - the model derived from S2 but where an initial binding to the assembly can be done ONLY if at least one matching glue exists (denoted as model S3 in the manuscript)
***********************************************************************************

To run the models one should install BioNetGen and NFsim, see the NFsim web-site (download):
http://michaelsneddon.net/nfsim/download/

For the result visualisation, the following guides are provided by the NFsim team (see the NFsim support page:)
http://michaelsneddon.net/nfsim/pages/support/support.html

"
How should I visualize simulation results?    

Standard simulation output is sent to a text file with the ".gdat" extension. This file is just a table of Observable counts at each time point, so you can plot the results in many different programs. NFsim comes with a simple Java based plotting program called PhiBPlot that reads "gdat" files. We also highly recommend using Matlab, where you can read in the file with the command:
[data,headers] = tblread(['filename']);
This will read the file and store the results in a matrix named data allowing you to use Matlab's powerful plotting tools. Of course, you can always import the file into Excel or write your own custom program as well.

NFsim also supports more complex output in the form of a complete system dump. The system dump allows you to get the entire state of the system at any specified time. Details on setting up a system dump is provided in the user manual. NFsim comes with a set of Matlab tools for automatically reading the output that are also described in the user manual.


" 

To run the models from this directory, enter the command prompt and change
directories to this folder.  Then call BioNetGen to generate an NFsim
readable XML file with the command:

   > perl ../../BNG/BNG2.pl kTAM_Classic_sierpinski_slot.bngl

Then, you can run the model by typing in mac or linux with the command:

  > ../../bin/NFsim_[version] -xml kTAM_Classic_sierpinski_slot.xml

Where [version] is the version of the NFsim executable, which will be
specific to your operating system.  In windows, type:

  > ../../bin/NFsim_[version].exe -xml kTAM_Classic_sierpinski_slot.xml

Again [version] is the version of your NFsim executable, which you will find 
in the "bin" directory.  For more help on running NFsim, or if you run into 
problems, consult the user manual available from the NFsim website.
