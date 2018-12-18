# celine-surprise.github.io

function init() {
Tabletop.init( { key: ‘1CMYY-zkB0x24fiM2LwqiaaUiG5QshgrH14mKembQuY0’,
callback: showInfo,
simpleSheet: true } )
}
function showInfo(data, tabletop) {
console.log(data);
for (var i = 0; i < data.length; i++) {
$(‘.post’).append(
‘<div class=”article” style=”background-image: url( ‘ +
data[i].img + ‘.jpg)”>’ +
‘<div class=”text”>’ +
‘<h1>’ + data[i].title + ‘</h1>’+
data[i].body +
‘</div> ‘ + ‘<div class=”meta-info”>’ + ‘<img src =”’ + data[i].img + ‘.jpg”>’+
‘<div class=”date”>’ + data[i].date + ‘</div>’ +
‘</div>’ +
‘</div>’);
}
}
window.addEventListener(‘DOMContentLoaded’, init)
