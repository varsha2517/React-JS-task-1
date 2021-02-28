<!-- <!DOCTYPE html>
<html>
<body>
<script type="text/javascript">
    function ShowHideDiv() {
        var Devices = document.getElementById("Devices");
        var sensorFields = document.getElementById("sensorFields");
        sensorFields.style.display = Devices.value == "sensor" ? "block" : "none";
		var motorFields = document.getElementById("motorFields");
        motorFields.style.display = Devices.value == "motor" ? "block" : "none";
		var relayFields = document.getElementById("relayFields");
        relayFields.style.display = Devices.value == "relay" ? "block" : "none";
		var selectModule = document.getElementById("selectModule");
		var contents;
		for(let i=1; i<=32; i++) {
		contents += "<option>" + i + "</option>";
		}
		selectModule.innerHTML = contents;
    }
</script>

    <select id = "Devices" onchange = "ShowHideDiv()">
		<option value="" disabled selected>Choose a Device</option>
        <option value="sensor">Sensor</option>
        <option value="motor">Motor</option>  
		<option value="relay">Relay</option>  	
    </select>
<hr />
<div id="sensorFields" style="display: none">
    Sensor Id:
    <input type="text" id="sensorId" />
    Sensor Name:
    <input type="text" id="sensorName" />
</div>
<div id="motorFields" style="display: none">
    Motor Id:
    <input type="text" id="motorId" />
    Motor Name:
    <input type="text" id="MotorName" />
</div>
<div id="relayFields" style="display: none">
    Relay Id:
    <input type="text" id="relayId" />
    Relay Name:
    <input type="text" id="relayName" />
	<select name="modules" id = "selectModule"></select>
</div>

</body>
</html> -->
<!DOCTYPE html>
<html>
    <script>
    function showMe(e) {
        var strdisplay = e.options[e.selectedIndex].value;
        console.log('strdisplay',strdisplay)
        var elementId = document.getElementById("elemId");
        var elementName = document.getElementById("elementName");
        var module = document.getElementById("module");
        console.log('elementId',elementId)
        console.log('elementName',elementName)
        if(strdisplay == "sensor") {
            elementId.placeholder = "Sensor Id";
            elementName.placeholder = "Sensor Name";
            module.style.display ="none";
            console.log('elementId',elementId)
            console.log('elementName',elementName)
        } else if(strdisplay == "motor") {
            elementId.placeholder = "Motor Id";
            elementName.placeholder = "Motor Name";
            module.style.display ="none";
            console.log('elementId',elementId)
            console.log('elementName',elementName)
        }else if(strdisplay == "relay") {

            elementId.placeholder = "Relay Id";
            elementName.placeholder = "Relay Name";
            module.style.display ="block";

            console.log('elementId',elementId)
            console.log('elementName',elementName)
        }
        function moduleInputDisplay(selected) {
            console.log("selected",selected)
            add(selected)
        }
        function add(type) {

        //Create an input type dynamically.
        var element = document.createElement("input");

        //Assign different attributes to the element.
        element.setAttribute("type", type);
        element.setAttribute("value", type);
        element.setAttribute("name", type);


        var foo = document.getElementById("fooBar");

        //Append the element in page (in span).
        foo.appendChild(element);

        }
    }</script>
<body>

<h1>Choose a Device from the available options</h1>

<form action="/action_page.php">
  <label for="cars">Choose Device</label>
  <select onchange ="showMe(this);" name="device" id="device">
    <option value="sensor">Sensor</option>
    <option value="motor">Motor</option>
    <option value="relay">Relay</option>
  </select>
  <br><br>
  <input id="elemId" type="text" placeholder="Sensor Id">
  <input id="elementName" type="text" placeholder="Sensor Name">
  <select style="display: none" onchange="moduleInputDisplay(this);" name="module" id="module">
    <option value="1">1</option>
    <option value="2">2</option>
    <option value="4">4</option>
    <option value="5">5</option>
    <option value="6">6</option>
    <option value="7">7</option>
    <option value="8">8</option>
    <option value="9">9</option>
    <option value="10">10</option>
    <option value="11">11</option>
    <option value="12">12</option>
    <option value="13">13</option>
    <option value="14">14</option>
    <option value="15">15</option>
    <option value="16">16</option>
    <option value="17">17</option>
    <option value="18">18</option>
    <option value="19">19</option>
    <option value="20">20</option>
    <option value="21">21</option>
    <option value="22">22</option>
    <option value="23">23</option>
    <option value="24">24</option>
    <option value="25">25</option>
    <option value="26">26</option>
    <option value="27">27</option>
    <option value="28">28</option>
    <option value="29">29</option>
    <option value="30">30</option>
    <option value="31">31</option>
    <option value="32">32</option>
  </select>
</form>

<p>Click the "Submit" button and the form-data will be sent to a page on the 
server called "action_page.php".</p>

</body>
</html>
