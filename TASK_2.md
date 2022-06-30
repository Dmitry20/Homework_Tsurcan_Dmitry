# Homework_INDROVO
Test Task
const K = 22;
const ARR = [44, -25, 1, 18, 24];

function findBestMatch(K, ARR) {
  // default values
  let nearest;
  let bestDistanceFound = Number.MAX_SAFE_INTEGER;;
  //iterate on array
  for (let i = 0; i < ARR.length; i++){
    // if we found our number we return it
    if (ARR[i] === K) {
      return ARR[i];
    //verify our actual distance and if its less than
    //current one we reassign it to a new value
    } else {
      let d = Math.abs(K - ARR[i]);
      if (d < bestDistanceFound) {
      bestDistanceFound = d; 
      //assign the value of array element 
      //according to our actual best distance
      nearest = ARR[i];
      }
    }
  }
  return nearest;
}

const bestMatch = findBestMatch(K, ARR);
console.log(bestMatch);
