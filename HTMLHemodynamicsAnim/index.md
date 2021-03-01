# Hemodynamics model simulator

Press buttons to start/stop/step/reset simulation:
<bdl-fmi id="idfmi" src="Physiolibrary_Fluid_Examples_Fernandez2013_PulsatileCirculation.js" fminame="Physiolibrary_Fluid_Examples_Fernandez2013_PulsatileCirculation" tolerance="0.000001" starttime="0" fstepsize="0.01" guid="{2bf08778-0486-4d6a-a11e-ad62e37621f7}" valuereferences="637534373" valuelabels="aorta.pressure" inputs="id1,16777337,1,60" inputlabels="heartRate.k"></bdl-fmi>

<bdl-range id="id1" title="Heart rate" min="30" max="180" default="60" step="1" maxlength="2"></bdl-range>

<bdl-chartjs-time id="id10" width="300" height="200" fromid="idfmi" labels="Aorta pressure" initialdata="" refindex="0" refvalues="1"></bdl-chartjs-time>