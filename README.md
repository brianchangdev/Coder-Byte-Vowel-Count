# Coder-Byte-Vowel-Count

Using the JavaScript language, have the function VowelCount(str) take the str       
string parameter being passed and return the number of vowels the string contains   
(ie. "All cows eat grass" would return 5). Do not count y as a vowel for this       
challenge

// go through string and check for vowels
// if vowel, then add to count
// return number of count

    function VowelCount(str){
    var vowel = ["a","e","i","o","u"];
    var count = 0;
      for(var i = 0; i < vowel.length; i++){
      for(var j = 0; j < str.length; j++){
        if(vowel[i] == str[j]){
	       count += 1;
        }
      }   
    }
	  return count;
    }
    console.log(VowelCount("hello my name is"));
    
/////////////////////////////////

RegEx solution using .test() method
// The test() method executes a search for a match between a regular expression and a specified string.
// Returns true or false.

    function VowelCount(str){
      var letters = str.split('');
      var count = 0;
      for(var i = 0; i < letters.length; i++){
        if(/[aeiou]/.test(letters[i])){
	        count += 1;
        }
      }
      return count;
    }
    console.log(VowelCount("All cows eat grass"));


