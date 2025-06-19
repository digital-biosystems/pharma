# Cell culture virus infection model simulation.
<div class="w3-row">
<div class="w3-twothird">

## Simulation
<bdl-fmi id="idfmi" mode="oneshot" src="CellCulture.js" fminame="CellCulture" tolerance="0.00000000001" starttime="0" stoptime="9" fstepsize="0.03" fpslimit="60" guid="{45a4051d-4ad1-4260-bad4-eee7c618aea2}" valuereferences="21,19,20,23,24" valuelabels="cell_live,cell_exposed,cell_infectious,cell_sick,cell_susceptible" inputs="incubation,84,1,1,f;infectious,85,1,1,f;diseased,83,1,1,f;mortality,81,1,1,f;contactrate,70,1,1,f" inputlabels="t_incubation,t_infectious,t_diseased,mortality,beta"></bdl-fmi>

<bdl-chartjs-time width="400" height="200" fromid="idfmi" labels="live,exposed,infectious,sick,susceptible" initialdata="" refindex="0" refvalues="5" responsive="true" maxdata="1024"></bdl-chartjs-time>

</div>
<div class="w3-third">

## Parameters
<bdl-range id="mortality" title="MOR" min="0" max="1" default="0.8" step="0.05"></bdl-range>

<bdl-range id="incubation" title="INC" min="0.1" max="5" default="1" step="0.1"></bdl-range>

<bdl-range id="infectious" title="INF" min="0.1" max="5" default="1" step="0.1"></bdl-range>

<bdl-range id="diseased" title="DIS" min="0.1" max="5" default="1" step="0.1"></bdl-range>

<bdl-range id="contactrate" title="CON" min="0.1" max="100" default="10" step="0.1"></bdl-range>

</div>
</div>