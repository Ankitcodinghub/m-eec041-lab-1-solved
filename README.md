# m-eec041-lab-1-solved
**TO GET THIS SOLUTION VISIT:** [M.EEC041 Lab 1 Solved](https://www.ankitcodinghub.com/product/m-eec041-lab-1-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94389&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;M.EEC041 Lab 1 Solved&nbsp;&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
In this exercise the students will be introduced to the digital simulation environment Questasim and review basic concepts of the hardware description language Verilog. After concluding this exercise the students should be able to:

</div>
</div>
<div class="layoutArea">
<div class="column">
<ol>
<li>setup a simulation project in Questasim and execute a basic simulation flow;</li>
<li>distinguish between the structure of Verilog models for supporting a simulation (testbenches) and the models that represent the digital circuit being verified or
the system under verification;
</li>
<li>identify the structure of basic Verilog design entities ( module(…)) and the
implementation of the interconnections among them.
</li>
<li>understand the structure of an elementary Verilog testbench module.</li>
</ol>
2. Project setup

For this lab you should download the archive PSD2022-T1.zip available in the contents section in the course web page. This archive contains 4 Verilog files placed in different folders, as referred below. Unpack the archive to a convenient location under your home directory (for example &lt;myfolder&gt;/psdi/labs/lab1/…)1, keeping the same folder hierarchy as in the original archive. Although this organization of files and folders is not mandatory, it is always a good practice to maintain the various files created during the development of a project organized in a convenient directory tree. For now, we will use the following tree structure:

&lt;root project dir&gt;

|–src (all source files)

| |–verilog (all Verilog files)

| | |–testbench (Verilog models for simulation only)

| | |–rtl (Verilog models for implementation)

| |–data (any additional source data files, not HDL) |–sim (simulation directory: create here the Questa project)

</div>
</div>
<div class="layoutArea">
<div class="column">
3.

</div>
<div class="column">
The system to simulate

</div>
</div>
<div class="layoutArea">
<div class="column">
The digital system to simulate in this lab consists in a UART transceiver (Universal Asynchronous Receiver/Transmitter) connected in loopback mode through a hardware implementation of the toupper() C function (convert lowercase letters to uppercase while any other characters are kept unchanged). The testbench model (lab1_tb.v) instantiates another UART (a simplified model, designed for simulation only) to simplify the generation of the simulation stimuli. Figure 1 represents a block diagram of the complete circuit that will be simulated in this exercise.

1 Do not use a directory tree that contains spaces or special characters in the directory names. Some design tools do not process correctly such names (as c:\ambiente de trabalho\utilizadores\…)

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
sim_uart.v

testbench (lab1_tb.v)

</div>
<div class="column">
uart.v

lab1.v (system under verification)

</div>
</div>
<div class="layoutArea">
<div class="column">
8 8

</div>
<div class="column">
8 8

</div>
</div>
<div class="layoutArea">
<div class="column">
dout din txen rxready

</div>
<div class="column">
tx rx

</div>
</div>
<div class="layoutArea">
<div class="column">
dout

rx

din

txen rxready

</div>
</div>
<div class="layoutArea">
<div class="column">
tx

</div>
</div>
<div class="layoutArea">
<div class="column">
toupper.v

</div>
</div>
<div class="layoutArea">
<div class="column">
1. Open the two Verilog files lab1_tb.v and lab1.v (use the text editor notepad++) and annotate the block diagram above with the names of the signals represented and add other signals not shown in the figure.

2. Execute QuestaSim and create a new project under folder ./sim. Add to the project the five Verilog files found under directories ./src/verilog/testbench (all sources related to testbenches) and ./src/verilog/rtl (the models that will be later implemented into a physical digital circuit – the reason for the designation “rtl” will be explained later)

3. Compile all Verilog files (accept all the default compilation options) and confirm that there are no compilation errors. The compilation process translates the Verilog files into a proprietary format and places the compiled models in the working user library (the default user library name is work and it is created as a folder under the project directory).

4. Start the simulation by selecting the model lab1_tb from the work library and executing the command “Simulate without optimization” (for now we will execute a non-optimized simulation to keep the names of the signals in the simulation environment, as this is necessary for exporting them to the waveform viewer). Open the waveform viewer by executing the command do wave_lab1.do in the command shell and run the simulation with the command Simulate-&gt;Run-&gt;Run –All (or executing in the shell run –all).

5. The testbench lab1_tb.v includes a Verilog task (similar to a C function) to automate the verification process. During the simulation some errors are wrongly reported. Analyze and interpret the simulation results observed in the waveform window and in the text window and explain why the error reported is not a real error and what is wrong with the verification procedure.

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Using Icarus Verilog and the waveform viewer GTKWave (free tools, open source)

Download and install Icarus Verilog from http://iverilog.icarus.com/home Download and install GTKWave from http://gtkwave.sourceforge.net/

(installation packages for Windows64 also available in Moodle)

Icarus Verilog does not have a graphical interface and is executed from the command line with a text only interface. To run a simulation execute at the shell prompt:

<pre>iverilog &lt;list of verilog files&gt;
</pre>
or

iverilog –c text_file_with_list_of_verilog_files -o output_file_name

This compiles the Verilog sources to an intermediate format in file a.out (default filename) or to the file name specified by option -o. The simulation is executed with the command:

vvp a.out

To dump the signal transitions to a file for later analysis, include in the Verilog top- level testbench the statement:

<pre>initial
begin
</pre>
$dumpfile(“mysimdata.vcd”);// The filename with the waveform data

$dumpvars(0, lab1_tb ); // The root node to dump end

To analyze the waveforms of the signals created during the simulation, run GTKWave and open the file specified in the Verilog function $dumpfile( ), in this example the file mysimdata.vcd

</div>
</div>
</div>
