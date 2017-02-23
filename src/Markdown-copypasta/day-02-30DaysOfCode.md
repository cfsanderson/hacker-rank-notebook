// Day 2: 30 Days of Code

'use strict';

var _input = '';
var _index = 0;
process.stdin.on('data', (data) => { _input += data; });
process.stdin.on('end', () => {
	_input = _input.split(new RegExp('[\n ]+'));
	main(+(_input[0]), +(_input[1]), +(_input[2]));    
});

function main(mealCost, tipPercent, taxPercent) {
  // Write your code here
  let tip = ((mealCost * tipPercent) / 100)
  let tax = ((mealCost * taxPercent) / 100)
  let total = mealCost + tip + tax
  let round = Math.round(total)
  // Use console.log() to print to stdout
  console.log(`The total meal cost is ${round} dollars.`)
}
