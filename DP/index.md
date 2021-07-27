
# **Simulátor mimotělního objemu ECMO**
<div class="w3-row">
<div class="w3-third">


<bdl-fmi id="idfmi" src="DP_0ferkl_0ECMO_ECMO8allBMR1.js" fminame="DP_0ferkl_0ECMO_ECMO8allBMR1" tolerance="0.000001" starttime="0" fstepsize="1" guid="{b9e728da-a413-4a53-9679-0e2fa15a641d}" valuereferences="905971252,905971206,905972888,905972934,905972781,637534226,637537649,100666723,905973139,905973963,905971310,637535872" valuelabels="pO2Arteries.partialPressure,pCO2Arteries.partialPressure,pO2Veins.partialPressure,pCO2Veins.partialPressure,flowMeasure2.volumeFlowRate,resistor1.volumeFlowRate,conductor2.volumeFlowRate,volumeFlowRate.V_flow,pH_Arteries.pH,pH_Veins.pH,pressureArterial.pressure,PressureVeins.pressure" inputs="id1,16777223,1,1,0;id2,16777226,1,60,0;id3,16777228,1,1000000,0;id4,16777227,1,1,0;id5,16777224,1.250102626409427e-07,1,0;id6,16777225,1.250102626409427e-07,1,0;id7,16777233,1,1,0;id8,16777234,1,60000,0;id9,16777235,1,1,0;id10,16777232,1,1,0" inputlabels="Shunts,RR,DV,TV,StarlingLeft,StarlingRight,RPM,SWEEP,FiO2,VAV"></bdl-fmi>

**Parametry pacienta**

<bdl-range id="id1" title="P-L zkraty" min="0" max="1" default="0.02" step="0.01" maxlength="10"></bdl-range>

<bdl-range id="id2" title="dechová frekvence" min="0" max="40" default="15" step="1" maxlength="10"></bdl-range>

<bdl-range id="id3" title="Objem mrtvého prostoru" min="150" max="500" default="150" step="10" maxlength="10"></bdl-range>

<bdl-range id="id5" title="Výkonost levého srdce" min="0" max="1.25" default="1" step="0.1" maxlength="10"></bdl-range>

<bdl-range id="id6" title="Výkonost pravého srdce" min="0" max="1.25" default="1" step="0.1" maxlength="10"></bdl-range>

**Parametry ECMO**

<bdl-range id="id7" title="Otáčky ECMO pumpy" min="0" max="7000" default="0" step="500" maxlength="10"></bdl-range>

<bdl-range id="id8" title="Sweep parametr" min="0" max="10" default="0" step="0.5" maxlength="10"></bdl-range>

<bdl-range id="id9" title="FiO2" min="0.21" max="1" default="0.21" step="0.01" maxlength="10"></bdl-range>



**Předpřipravené scénáře**

<bdl-buttonparams title="zdravý pacient" ids="id1,id2,id3,id4,id5,id6,id7,id8,id9" values="0.02,15,500,150,1,1,0,0,0.21"></bdl-buttonparams>
<bdl-buttonparams title="Respirační selhání" ids="id1,id3" values="0.4,260"></bdl-buttonparams>
<bdl-buttonparams title="Srdeční selhání" ids="id5,id6" values="0.1,0.1"></bdl-buttonparams>

<bdl-buttonparams title="VA Zapojení" ids="id10,id7,id8,id9" values="1,4500,4500,0.5"></bdl-buttonparams>
<bdl-buttonparams title="VA Zapojení" ids="id10,id7,id8,id9" values="0,5000,3,0.8"></bdl-buttonparams>

</div>
<div class="w3-twothird">

<bdl-chartjs-time id="id100" width="700" height="500" fromid="idfmi" labels="pO2 Arterie (mmHg), pCO2 Arterie (mmHg),pO2 Vény (mmHg), pCO2 Vény (mmHg)" initialdata="" refindex="0" refvalues="4" convertors="x*0.00750061683;x*0.00750061683;x*0.00750061683;x*0.00750061683"></bdl-chartjs-time>

<bdl-chartjs-time id="id101" width="700" height="500" fromid="idfmi" labels="srdeční výdej, průtok arterie, Sweep, ECMO krev" initialdata="" refindex="4" refvalues="4" convertors="x*60*1000;x*60*1000;x*60*1000,x*60*1000"></bdl-chartjs-time>

<bdl-chartjs-time id="id102" width="700" height="500" fromid="idfmi" labels="pH krve" initialdata="" refindex="8" refvalues="1"></bdl-chartjs-time>


<bdl-chartjs-time id="id103" width="700" height="500" fromid="idfmi" labels="Střední arteriální tlak, Střední venózní tlak" initialdata="" refindex="10" refvalues="2" convertors="x*0.00750061683;x*0.00750061683"></bdl-chartjs-time>




</div>
</div>

