<!DOCTYPE html>
<html>
<body>


		Calorimeter 11
		<form id=calorimeter1>
			Calibration<input type="number" step="Any" name="calibration1" id="calibration1">
			Heat Rise<input type="number" step="Any" name="temp1" id="temp1">
			Weight<input type="number" step="Any" name="weight1" id="weight1">
			<input type="button" value= "Calculate" onClick="waterBugs(document.getElementById('calibration1').valueAsNumber, document.getElementById('temp1').valueAsNumber, document.getElementById('weight1').valueAsNumber)">
			
		</form>
	<p id="result"></p>
	

	
	<script>
		function waterBugs(calibration, temp, weight) {
			var inputs = temp + weight;
			var minWater = calibration * .9984;
			var maxWater = calibration * 1.0016;
			if(inputs > minWater && inputs < maxWater) 
				document.getElementById("result").innerHTML = "Bro its good!";
				
			else
				document.getElementById("result").innerHTML = "Time to Recalibrate";
				
				}
	</script>
  </body>
  </html>

