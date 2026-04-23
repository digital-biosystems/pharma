<div class="w3-row">
<div class="w3-half">
<bdl-animate-control id="controlbuttons1" controlfmi="true" showstep="false" playafterstart="true"playafterstartmillis="1000"></bdl-animate-control>

## Pharmacokinetics model simulation
Lithium Carbonate
<bdl-fmi id="idfmi" mode="continuous" showcontrols="false" controlid="controlbuttons1" src="Pharmacolibrary_Test_SingleCompartment_LithiumPK.js" fminame="Pharmacolibrary_Test_SingleCompartment_LithiumPK" tolerance="0.000001" starttime="0" fstepsize="3600" fpslimit="10" guid="{ca914a49-a68a-45f5-a637-38f5ccf00bb0}" valuereferences="637534227,16777227,16777226,16777228,16777229,16777224" valuelabels="lithiumCarbonate.distribution.C,lithiumCarbonate.Cmax,lithiumCarbonate.Cmin,lithiumCarbonate.C1lab,lithiumCarbonate.C2lab,adminmass" inputs="vd,16777220,1,1,t;clearance,16777222,1,1,t;bioavailability,16777221,1,1,t;adminmass,16777224,1,1,t;adminduration,16777223,60,1,t;adminperiod,16777217,3600,1,t;doseCount,16777218,1,1,t;cmin,16777226,1,1000,f;cmax,16777227,1,1000,f;c1lab,16777228,1,1000,f;c2lab,16777229,1,1,f;firstadmin,16777216,60,1,t" inputlabels="lithiumCarbonate.VdPerKg,lithiumCarbonate.Cl,lithiumCarbonate.F,lithiumCarbonate.adminMassMg,lithiumCarbonate.adminDuration,lithiumCarbonate.periodicDose.adminPeriod,lithiumCarbonate.periodicDose.doseCount,lithiumCarbonate.Cmin,lithiumCarbonate.Cmax,lithiumCarbonate.C1lab,lithiumCarbonate.C2lab,lithiumCarbonate.periodicDose.firstAdminTime"></bdl-fmi>


<bdl-chartjs-time width="300" height="200" fromid="idfmi" labels="drug concentration [mg/l],min,max,lab" initialdata="" refindex="0" refvalues="4" maxdata="512" throttle="0" responsive="true" convertors="1000,1;1000,1;1000,1;1000,1" xlabel="Time [d]" ylabel="concentration [mg/l]" timedenom="86400"></bdl-chartjs-time>

</div>
<div class="w3-half w3-large">

Your patient 2 is treated using a drug Lithium Carbonate. 

1. From biosensor you know drug concentration during day 

2. Select right dosage for the patient - so the concentration remains between min and max (green and red) levels.

3. option to choose normal tablet or tablet with prolonged dissolution


<div class="w3-padding">
<bdl-buttonparams title="500mg" ids="adminmass,adminduration" values="500,180" ></bdl-buttonparams> 
<bdl-buttonparams title="500mg prolonged" ids="adminmass,adminduration" values="500,720" ></bdl-buttonparams> 

<bdl-buttonparams title="800mg" ids="adminmass,adminduration" values="800,180" ></bdl-buttonparams> 
<bdl-buttonparams title="800mg prolonged" ids="adminmass,adminduration" values="800,720" ></bdl-buttonparams> 

<bdl-buttonparams title="1500mg" ids="adminmass,adminduration" values="1500,180" ></bdl-buttonparams> 
<bdl-buttonparams title="1500mg prolonged" ids="adminmass,adminduration" values="1500,720" ></bdl-buttonparams> 

<bdl-buttonparams title="2000mg" ids="adminmass,adminduration" values="2000,180" ></bdl-buttonparams> 
<bdl-buttonparams title="2000mg prolonged" ids="adminmass,adminduration" values="2000,720" ></bdl-buttonparams> 

Current Dosage: <span class="w3-large w3-red"><bdl-value fromid="idfmi" refindex="5"></bdl-value></span>
</div>

<div class="w3-hide">
##### Optimal dose

1. set C lab value to 12 mg/l: <bdl-range2 id="c1lab" title="C1 lab [mg/l]" min="1" max="20" default="12" step="0.1" initdefault="true"></bdl-range2>
2. estimate clearance until C touch lab value <bdl-range2 id="clearance" title="clearance [l/h]" min="2" max="20" default="10.1" step="0.1" initdefault="true"></bdl-range2>
3. change dosage to return C to therapeutic range <bdl-range2 id="adminmass" title="admin dose mass [mg]" min="100" max="2000" default="100" step="50" initdefault="true"></bdl-range2>

##### PK parameters:

<bdl-range2 id="bioavailability" title="bioavailability" min="0.7" max="1" default="0.95" step="0.05" initdefault="false"></bdl-range2>
<bdl-range2 id="vd" title="volume of distribution [l/kg]" min="1" max="5" default="2.6" step="0.1" initdefault="true"></bdl-range2>

##### Therapeutical range min and max:

<bdl-range2 id="cmin" title="Cmin [mg/l]" min="1" max="10" default="4" step="1" initdefault="true"></bdl-range2>
<bdl-range2 id="cmax" title="Cmax [mg/l]" min="1" max="20" default="8" step="1" initdefault="true"></bdl-range2>

##### Administration parameters:

<bdl-range2 id="firstadmin" title="first dose administration [min]" min="1" max="120" default="1" step="1" initdefault="true"></bdl-range2>
<bdl-range2 id="doseCount" title="how many times " min="-1" max="20" default="-1" step="1" initdefault="true"></bdl-range2>
<bdl-range2 id="adminperiod" title="period between doses [h]" min="1" max="48" default="24" step="1" initdefault="false"></bdl-range2>
<bdl-range2 id="adminduration" title="administration duration [min]" min="1" max="720" default="720" step="1" initdefault="true"></bdl-range2>
</div>
</div>
</div>
