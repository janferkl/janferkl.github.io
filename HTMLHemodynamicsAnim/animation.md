# Heart during cardiac cycle

<div class="w3-row">
<div class="w3-twothird">

## simulation and chart

Press buttons to start/stop/step/reset simulation:
<bdl-fmi id="idfmi" src="Physiolibrary_Fluid_Examples_Fernandez2013_PulsatileCirculation.js" fminame="Physiolibrary_Fluid_Examples_Fernandez2013_PulsatileCirculation" tolerance="0.000001" starttime="0" fstepsize="0.01" guid="{2bf08778-0486-4d6a-a11e-ad62e37621f7}" valuereferences="637534373,637534289,637534350,637534462,637534521,637534315,637534487" valuelabels="aorta.pressure,mitralValve.open,aorticValve.open,tricuspidValve.open,pulmonaryValve.open,leftVentricle.volume,rightVentricle.volume" inputs="id1,16777337,1,60" inputlabels="heartRate.k"></bdl-fmi>




<bdl-range id="id1" title="Heart rate" min="30" max="180" default="60" step="1" maxlength="2"></bdl-range>


<bdl-chartjs-time id="id10" width="300" height="200" fromid="idfmi" labels="Aorta pressure [mmHg]" initialdata="" refindex="0" refvalues="1" convertors="x/133.322-760" ></bdl-chartjs-time>

</div>
<div class="w3-third">

## animation
<bdl-animate-adobe src="CardiaccycleStage.js" width="200" height="200" name="Faze_srdce" fromid="idfmi"></bdl-animate-adobe>

<bdl-bind2a findex="1" aname="ValveMV_anim" amin="99" amax="0" fmin="0" fmax="1"></bdl-bind2a>

<bdl-bind2a findex="2" aname="ValveAOV_anim" amin="0" amax="99" fmin="0" fmax="1"></bdl-bind2a>

<bdl-bind2a findex="3" aname="ValveTV_anim" amin="99" amax="0" fmin="0" fmax="1"></bdl-bind2a>

<bdl-bind2a findex="4" aname="ValvePV_anim" amin="0" amax="99" fmin="0" fmax="1"></bdl-bind2a>

<bdl-bind2a findex="5" aname="ventricles.ventriclesTotal.VentricleLeft_anim" amin="100" amax="0" fmin="0.00015" fmax="0.00021"></bdl-bind2a>

<bdl-bind2a findex="6" aname="ventricles.ventriclesTotal.children.0.VentricleRight_anim" amin="100" amax="0" fmin="0.00012" fmax="0.00018"></bdl-bind2a>


</div>
</div>