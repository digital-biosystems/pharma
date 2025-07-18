<div class="w3-row">
<div class="w3-third">

# Remdesivir PK

Simulation of pharmacokinetic and drug concentration.
<bdl-fmi id="idfmi" mode="oneshot" src="RemdesivirPK.js" fminame="RemdesivirPK" tolerance="0.000001" starttime="0" stoptime="864000" fstepsize="1000" fpslimit="60" guid="{8d5e8c78-9841-471d-a354-4e3c0f8c6e6a}" valuereferences="10,17,16,34,10,11" valuelabels="remdesivir.distribution.C,remdesivir.Cmin,remdesivir.Cmaxremdesivir.absorption.drugAdministered.C0,remdesivir.elimination.C,remdesivir.distribution.absorptionFlow" inputs="vd,20,1,1,f;clearance,15,1,1,f;bioavailability,18,1,1,f;adminmass,23,1,1,f;adminduration,40,60,1,f;doseCount,2,1,1,f;cmin,17,1,1,f;cmax,16,1,1,f;firstadmin,28,60,1,f" inputlabels="remdesivir.VdPerKg,remdesivir.Cl,remdesivir.F,remdesivir.absorption.adminMassMg,remdesivir.adminDuration,remdesivir.absorption.dose.doseCount,remdesivir.Cmin,remdesivir.Cmax,remdesivir.absorption.dose.firstAdminTime"></bdl-fmi>

<bdl-chartjs-time width="400" height="300" fromid="idfmi" labels="drug concentration [g/l],min,max,lab" initialdata="" refindex="0" refvalues="4" maxdata="10192" throttle="50"></bdl-chartjs-time>

</div>
<div class="w3-third">

One compartment model parameters:

<bdl-range id="bioavailability" title="bioavailability" min="0.8" max="1" default="0.95" step="0.05" initdefault="false"></bdl-range><br/>
<bdl-range id="vd" title="volume of distribution [l/kg]" min="1" max="5" default="3" step="0.1" initdefault="false"></bdl-range><br/>
<bdl-range id="clearance" title="clearance [l/h]" min="2" max="20" default="9.4" step="0.1" initdefault="false"></bdl-range><br/>

Therapeutical range min and max:

<bdl-range id="cmin" title="Cmin [g/l]" min="0.001" max="0.01" default="0.004" step="0.001" initdefault="false"></bdl-range><br/>
<bdl-range id="cmax" title="Cmax [g/l]" min="0.001" max="0.02" default="0.008" step="0.001" initdefault="false"></bdl-range><br/>
<br/>
<bdl-range id="c1lab" title="C1 lab [g/l]" min="0.001" max="0.02" default="0.008" step="0.001" initdefault="false"></bdl-range><br/>
<br/>

Dose administration parameters:

<bdl-range id="adminmass" title="admin dose mass [mg]" min="500" max="2000" default="1500" step="100" initdefault="false"></bdl-range><br/>
<bdl-range id="firstadmin" title="first dose administration [min]" min="30" max="120" default="30" step="10" initdefault="false"></bdl-range><br/>
<bdl-range id="admincount" title="how many times " min="1" max="21" default="10" step="1" initdefault="false"></bdl-range><br/>
<bdl-range id="adminperiod" title="period between doses [h]" min="1" max="48" default="24" step="1" initdefault="false"></bdl-range><br/>
<bdl-range id="adminduration" title="administration duration [min]" min="1" max="720" default="720" step="1" initdefault="false"></bdl-range><br/>
<!--bdl-fmi id="idfmi" mode="oneshot" src="Pharmacolibrary_Test_SingleCompartment_LithiumPK.js" fminame="Pharmacolibrary_Test_SingleCompartment_LithiumPK" tolerance="0.000001" starttime="0" fstepsize="1000" stoptime="864000" fpslimit="60" guid="{ca914a49-a68a-45f5-a637-38f5ccf00bb0}" valuereferences="637534227,16777227,16777226,16777228,16777229" valuelabels="lithiumCarbonate.distribution.C,lithiumCarbonate.Cmax,lithiumCarbonate.Cmin,lithiumCarbonate.C1lab,lithiumCarbonate.C2lab" inputs="vd,16777220,1,1,t;clearance,16777222,1,1,t;bioavailability,16777221,1,1,t;adminmass,16777224,1,1,t;adminduration,16777223,60,1,t;adminperiod,16777217,3600,1,t;doseCount,16777218,1,1,t;cmin,16777226,1,1,f;cmax,16777227,1,1,f;c1lab,16777228,1,1,f;c2lab,16777229,1,1,f;firstadmin,16777216,60,1,t" inputlabels="lithiumCarbonate.VdPerKg,lithiumCarbonate.Cl,lithiumCarbonate.F,lithiumCarbonate.adminMassMg,lithiumCarbonate.adminDuration,lithiumCarbonate.periodicDose.adminPeriod,lithiumCarbonate.periodicDose.doseCount,lithiumCarbonate.Cmin,lithiumCarbonate.Cmax,lithiumCarbonate.C1lab,lithiumCarbonate.C2lab,lithiumCarbonate.periodicDose.firstAdminTime"></bdl-fmi-->

</div>
<div class="w3-third w3-xlarge w3-padding">
Instructions

1. Measured concentration of drug in plasma was 0.012 g/l. Set <b>C1 lab</b> to this value.
2. Patient has renal insufficiency with creatinine conc in plasma 130 mmol/l. Estimate renal clearance by modifying the <b>clearance</b>. Match peak simulated concentration to C1 lab level.
3. Adjust <b>administration dose mass</b> to fit inside therapeutic level.       


</div>
</div>