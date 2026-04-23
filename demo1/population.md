<div class="w3-row">
<div class="w3-twothird">

# Epidemiological model of infection spread

SEIRSD with additional admitance and hospitalization

<bdl-fmi id="idfmi" mode="oneshot" src="Covid_SEIRS_Ext.js" fminame="Covid_SEIRS_Ext" tolerance="0.0000001" starttime="0" stoptime="183" fstepsize="1" fpslimit="60" guid="{271e00f6-4cc7-4209-8953-7274d2ab6f08}" valuereferences="6,1,3,4,0,5,2" valuelabels="Susceptible.population,Exposed.population,Infectious.population,Recovered.population,Dead.population,Sick.population,Hospitalized.population" inputs="incubation,130,1,1,f;infectious,131,1,1,f;beta,104,1,1,f" inputlabels="t_incubation,t_infectious,beta"></bdl-fmi>

<bdl-chartjs-time width="600" height="400" fromid="idfmi" labels="susceptible,exposed,infectious,recovered,dead,sick" initialdata="" refindex="0" refvalues="6" responsive="true" maxdata="512"></bdl-chartjs-time>
<bdl-chartjs-time width="600" height="100" fromid="idfmi" labels="hospitalized" initialdata="" refindex="6" refvalues="1" responsive="true" maxdata="512"></bdl-chartjs-time>

</div>
<div class="w3-third">

<bdl-range id="incubation" title="Incubation [d]" min="0.1" max="10" default="5" step="0.1" initdefault="false"></bdl-range>

<bdl-range id="infectious" title="Infectious [d]" min="0.1" max="10" default="2" step="0.1" initdefault="false"></bdl-range>

<bdl-range id="beta" title="Contact Rate" min="0.1" max="10" default="1.75" step="0.05" initdefault="false"></bdl-range>
</div>
</div>

