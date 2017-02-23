// Day 3: 30 Days of Code

process.stdin.resume();
process.stdin.setEncoding('ascii');

var input_stdin = "";
var input_stdin_array = "";
var input_currentline = 0;

process.stdin.on('data', function (data) {
    input_stdin += data;
});

process.stdin.on('end', function () {
    input_stdin_array = input_stdin.split("\n");
    main();    
});

function readLine() {
    return input_stdin_array[input_currentline++];
}

/////////////// ignore above this line ////////////////////

function main() {
    var N = parseInt(readLine());
    if (N % 2 != 0) {
      console.log('Weird')
// If N is odd, print Weird
    } else if (N % 2 === 0 && N > 20) {
      console.log('Not Weird')
// If N is even and greater than 20, print Not Weird
    } else if (N % 2 === 0 && N >= 2 && N <= 5) {
      console.log('Not Weird')
// If N is even and in the inclusive range of 2 to 5, print Not Weird
    } else if (N % 2 === 0 && N >= 6 && N <= 20) {
      console.log('Weird')
// If N is even and in the inclusive range of 6 to 20, print Weird
    }
}
