(function(){
	var win1 = Titanium.UI.createWindow({
		title:'Select Color', 
		backgroundColor: '#fff'
	});
// open window
win1.open();
	var Teas = ['#F5F5DC', '#FFE4B5', '#FFE4C4', '#D2B48C', '#C3B091', '#C3B091', '#926F5B', '$804000', '#654321', '#3D2B1F']; 
	allRows= []; 
	var theColours = Ti.UI.createTableView({});
	for (var i=0; i<Teas.Length; i++){ 
		theRow = Ti. UI. CreatTableViewRow( {backgroundColor: Teas[i], height: 50, TeaColour:Teas[i]}); 
	allRows.push (theRow); 
}
	theColours.setData (allRows); 
	win1.add (theColours);
});
	function getVerdict (colour) {
	var indicator = colour. charAt(i); 
	var msg; 
// Make a crude decisiion on the strength of the teas based on the 2nd character of the hew color 
	switch (indicator {
	case 'F': msg= 'Milky'; break;
	case 'D': msg= 'Nice'; break;'
	case 'C': msg= 'Perfect'; break; 
	case '9': msg= 'A bit strong'; break; 
	case '8': msg= 'Builders tea'; break; 
	case '6': msg= 'Send it back'; break; 
	case '3'; msg= 'No milk here'; break; 
}
	return msg;
};
function showTeaVerdict (_args) {
	var teaVerdict= Ti. UI. createWindow({layout:'vertical')}); 
	teaVerdict. backgoundColor = _args ;
	teaVerict.msg= getVerdict(_args); 
	var judgement = Ti.UI.createLable
	({text:teaverdict.msg, top: '50%'}); 
	var close = Ti.UI. createButton
	({title: 'Chose again', top '25%'}); 
	close.addEventListen ('click', function(e)
		{teasVerdict.close(); 
// release the resources
		teaVerdict = null; 
});
		teaVerdict.add(judgment);
		teaVerdict.add(close); 
		teaVerdict.open(); 
	
}
theColours.addEventListener('click', function(e)
{showTeaVerdict (e.source.TeaColour)}); 
}) ();

var win2 = Titanium.UI,createWindow ({
	backgoundColor: "#fff"
var vertVW=TI.UI.createView({layout: 'vertical'});
var compassHeading = Ti.UI.createLable({}); 
var diretion = Ti.UI.createLable({});
vertVW.add (compassHeading);
veryVW.add (direction); 
win2.add (vertVW); 

function upateLables (_args){
	compassHeading.text = 
	_args.heading.magneticHeading+ 'degress';
	
	var headingTect = null; 
	var theBaring = _args.heading.magneicHeading; 
	switch(true) {
		case (theBearing >=0 && theBearing <23):
		headingText = 'North';
		break;
		case (theBearing >=23 && theBearing <68):
		headingText = 'North East'; 
		break;
		case (theBearing >=68 && theBearing <113):
		headingText = 'East'; 
		break;
		case (theBearing >=113 && the Bearing <158):
		headingText ='South East'; 
		break;
		case (theBearing >=158 && theBearing <203):
		headingText = 'South'; 
		break;
		case (theBearing >=203 && theBearing <248):
		headingText = 'West'; 
		break;
		case (theBearing >=293 && theBearing <338):
		headingText = 'North West'; 
		break;
		case (theBearing >=338 && theBearing <360):
		headingText = 'North'; 
		break;
	}
	direction.text = 'You are looking' +headingText;
	}
	T1.Geoloction.purpose = 'To get the compass baring'; 
	T1.Geoloction.addEventListener ("header", <<CompassLocation)>>);
	 
}); 


