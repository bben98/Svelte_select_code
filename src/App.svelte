

  <select bind:value={selected}>
    {#each time as times}
      <option value={times}>{times}</option> 
    {/each}
    
  </select>
  <p>{options.markers == reallocation[0]}</p>
<p>{central == reallocation[0][0]}</p>
<p>{JSON.stringify(options)}</p>
<p>{finalloc}</p>

<script>
    import Select from 'svelte-select';
    import Map from '@anoram/leaflet-svelte'
    export const trial = [{"latitude":13.715647305348398,"longitude":100.5584224689399,"time":1614221982},{"latitude":13.717667933333333,"longitude":100.55816078333335,"time":1614221954},{"latitude":13.719766653875542,"longitude":100.55780022841442,"time":1614221669},{"latitude":13.72130865,"longitude":100.55645416666667,"time":1614221625},{"latitude":13.722304383333336,"longitude":100.55416343333331,"time":1614221587},{"latitude":13.7231023,"longitude":100.55226223333332,"time":1614221550},{"latitude":13.723877916666668,"longitude":100.55028803333335,"time":1614221514},{"latitude":13.72462732159947,"longitude":100.5484923207071,"time":1614221484},{"latitude":13.725411000000001,"longitude":100.54649561666665,"time":1614221472},{"latitude":13.726242206367122,"longitude":100.54459621320571,"time":1614221460},{"latitude":13.726985283629789,"longitude":100.5427978761888,"time":1614221448},{"latitude":13.727767183333333,"longitude":100.54096996666667,"time":1614221436},{"latitude":13.728506233333333,"longitude":100.5391892,"time":1614221426},{"latitude":13.72937306666667,"longitude":100.53713590000001,"time":1614221416},{"latitude":13.730202450000002,"longitude":100.53511581666667,"time":1614221406},{"latitude":13.73107891666667,"longitude":100.53303611666668,"time":1614221394},{"latitude":13.731880633333333,"longitude":100.53115671666667,"time":1614221382},{"latitude":13.732803116666664,"longitude":100.52917351666669,"time":1614221368},{"latitude":13.733720768976665,"longitude":100.52730329299791,"time":1614208032},{"latitude":13.735046533333332,"longitude":100.52876266666665,"time":1614207925},{"latitude":13.7330906,"longitude":100.52867816666667,"time":1614207890},{"latitude":13.732197413087608,"longitude":100.52688987525404,"time":1614207774},{"latitude":13.7318491,"longitude":100.5249075,"time":1614207738},{"latitude":13.7314783,"longitude":100.52287810000001,"time":1614207719},{"latitude":13.731084883333331,"longitude":100.52088365,"time":1614207702},{"latitude":13.730727833333333,"longitude":100.5187545,"time":1614207683},{"latitude":13.729838533333334,"longitude":100.51569018333332,"time":1614207649},{"latitude":13.7279211,"longitude":100.51596113333332,"time":1614207631},{"latitude":13.725900581930825,"longitude":100.51620970811537,"time":1614207614},{"latitude":13.724368783333333,"longitude":100.51753963333334,"time":1614207551},{"latitude":13.722337179395897,"longitude":100.51785625941825,"time":1614207532},{"latitude":13.720340600000002,"longitude":100.51838703333333,"time":1614207496},{"latitude":13.7183325,"longitude":100.51770915000002,"time":1614207467},{"latitude":13.718533983333336,"longitude":100.51568105,"time":1614207440},{"latitude":13.719108249999998,"longitude":100.51355854999998,"time":1614207409},{"latitude":13.719602333333334,"longitude":100.51155041666668,"time":1614207387},{"latitude":13.720042049999998,"longitude":100.50963126666666,"time":1614207365},{"latitude":13.72059533333333,"longitude":100.50750128333333,"time":1614207350},{"latitude":13.72094451666667,"longitude":100.50550146666667,"time":1614207335},{"latitude":13.721110316666666,"longitude":100.50172730000001,"time":1614207310},{"latitude":13.721183699999997,"longitude":100.49977251666665,"time":1614207298},{"latitude":13.721187443190596,"longitude":100.49771638730554,"time":1614207286},{"latitude":13.721220633333333,"longitude":100.49548754999999,"time":1614207274},{"latitude":13.72111445,"longitude":100.49325038333333,"time":1614207262},{"latitude":13.72083061666667,"longitude":100.49128815,"time":1614207250},{"latitude":13.720432066666667,"longitude":100.48937554999998,"time":1614207238},{"latitude":13.719719000000001,"longitude":100.48736698333333,"time":1614207226},{"latitude":13.719185650000002,"longitude":100.48523533333334,"time":1614207212},{"latitude":13.718492166666666,"longitude":100.48338548333334,"time":1614207198},{"latitude":13.717552583333335,"longitude":100.48169455,"time":1614207186},{"latitude":13.716496133333333,"longitude":100.4797876,"time":1614207174},{"latitude":13.715475849999999,"longitude":100.47795288333333,"time":1614207162},{"latitude":13.714468066666667,"longitude":100.47625336666665,"time":1614207150},{"latitude":13.713226550000002,"longitude":100.47454158333333,"time":1614207138},{"latitude":13.712440283333335,"longitude":100.47275181666667,"time":1614207126},{"latitude":13.712710466666666,"longitude":100.47061825,"time":1614207110},{"latitude":13.7134652,"longitude":100.46871906666665,"time":1614207096},{"latitude":13.7142567,"longitude":100.46671636666666,"time":1614207079},{"latitude":13.714632116666667,"longitude":100.46471796666668,"time":1614207061},{"latitude":13.714092200000001,"longitude":100.46266696666667,"time":1614207047},{"latitude":13.713246800000002,"longitude":100.46085630000002,"time":1614207035},{"latitude":13.712397133333331,"longitude":100.45905721666668,"time":1614207021},{"latitude":13.71156275,"longitude":100.45727298333334,"time":1614207009},{"latitude":13.710747233333331,"longitude":100.45548383333336,"time":1614206997},{"latitude":13.709862400000002,"longitude":100.45368546666664,"time":1614206983},{"latitude":13.7088012,"longitude":100.45178463333332,"time":1614206967},{"latitude":13.707659533333333,"longitude":100.45013949999999,"time":1614206953},{"latitude":13.706330099999997,"longitude":100.44851816666666,"time":1614206939},{"latitude":13.7050133,"longitude":100.44711541666665,"time":1614206925},{"latitude":13.703527916666667,"longitude":100.44571198333333,"time":1614206911},{"latitude":13.702119583333335,"longitude":100.44438905000001,"time":1614206899},{"latitude":13.700646583333333,"longitude":100.44301681666666,"time":1614206887},{"latitude":13.699034733333333,"longitude":100.44152975,"time":1614206875},{"latitude":13.697462316666666,"longitude":100.44008861666669,"time":1614206858},{"latitude":13.695886366666665,"longitude":100.43863135000002,"time":1614206844},{"latitude":13.694299650000001,"longitude":100.43715963333334,"time":1614206833},{"latitude":13.692917466666664,"longitude":100.43584941666667,"time":1614206825},{"latitude":13.691591433333334,"longitude":100.43433791666666,"time":1614206816},{"latitude":13.690343749999998,"longitude":100.4328041,"time":1614206806},{"latitude":13.68914165,"longitude":100.43090378333332,"time":1614206792},{"latitude":13.688371299999998,"longitude":100.429145,"time":1614206782},{"latitude":13.6874057,"longitude":100.42728663333334,"time":1614206772},{"latitude":13.686447116666667,"longitude":100.42542285,"time":1614206762},{"latitude":13.685465166666667,"longitude":100.42356541666668,"time":1614206752},{"latitude":13.684591483333334,"longitude":100.42174938333334,"time":1614206743},{"latitude":13.683895749999998,"longitude":100.41981341666667,"time":1614206734},{"latitude":13.683444116666665,"longitude":100.4179305,"time":1614206726},{"latitude":13.6831534,"longitude":100.41598568333332,"time":1614206717},{"latitude":13.683115627580246,"longitude":100.41384536982197,"time":1614206705},{"latitude":13.683240750000001,"longitude":100.41172948333333,"time":1614206693},{"latitude":13.68357105,"longitude":100.40948606666667,"time":1614206681},{"latitude":13.684982600000001,"longitude":100.40774981666667,"time":1614206669},{"latitude":13.686912216666666,"longitude":100.40749856666669,"time":1614206657},{"latitude":13.688881266666666,"longitude":100.40753418333334,"time":1614206641},{"latitude":13.691089066666665,"longitude":100.40766363333331,"time":1614206629},{"latitude":13.693128283333333,"longitude":100.40772771666667,"time":1615206616},{"latitude":13.695122916666666,"longitude":100.40767820000002,"time":1615206606},{"latitude":13.697144733333335,"longitude":100.40747735000002,"time":1615206597},{"latitude":13.699134499999998,"longitude":100.40724965,"time":1615206589},{"latitude":13.701223483333335,"longitude":100.40701845,"time":1615206580}];
    export const timer = [];
    for(var i = 0; i < trial.length; i++){
        const milliseconds = trial[i]['time'] * 1000
        const dateObject = new Date(milliseconds)
        timer.push(dateObject.toLocaleString())
   }
	
    export const reallocation = [[[JSON.stringify(trial[0]['latitude']), JSON.stringify(trial[0]['longitude'])]]];
    export const realtime = [[timer[0]]];
    for(var i = 1; i < timer.length; i++){
      for (var j=0, k=false; j < realtime.length;j++){
          if (timer[i].substring(0,9) == realtime[j][0].substring(0,9)){
            realtime[j].push(timer[i]);
            reallocation[j].push([JSON.stringify(trial[i]['latitude']), JSON.stringify(trial[i]['longitude'])]);
            k=true;
            break;
          }
          if(j == realtime.length-1 && !k) {
            realtime.push([timer[i]]);
            reallocation.push([[JSON.stringify(trial[i]['latitude']), JSON.stringify(trial[i]['longitude'])]]);
          }
    }
  }
    var time = [];
    for (var i = 0; i < reallocation.length; i++){
      time[i] = realtime[i][0].substring(0,9).replace(/,/g, '');
    }


  let selected;
  let central = [];
  var finalloc = [];
  let options;
  //$: num;    
  
  $: for (var i = 0; i < time.length;i++){
    if (selected == time[i])
    {
      finalloc[0] = reallocation[i];
      break;
    }
  }
  finalloc = finalloc;
  //finalloc = finalloc;
  //finalloc.push(reallocation[i]);
  //export const central = markerLocations[0][Math.floor(Math.random() * markerLocations.length)];
  //var num = 0;
  $: options={
      center: reallocation[0][0],
      markers: finalloc,
      timer: time,
      mapID: "map"
    }
    
  $: options = options;
  //alert(opitions)
    </script>
 <style>
  .map {
    height: 600px;
    width: auto;
  }
</style>
{#if options != null}
<div class="map">
  <Map {options} />
</div>
{/if}


