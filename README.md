# laravel-wordcounter
Simple word counter for counting words from HTML but can be used for other text

## Installation

Add in your composer.json:

    {
        "require": {
            "MadTechie3000/laravel-wordcounter": "1.*"
        }
    }

Then you need run the `composer update` command.

## Use

**Important**: For documentation purposes, in the examples below, always we assume than you import the library into your namespace using `use MadTechie3000\laravel-wordcounter;`

    $wordcounter = new WordCounter;
    
    $total = $wordcounter->load('some text')
      ->countTotalWords()
    ;

    // Count each word
    // You receive an array with objects:
    $words = $wordcounter->load('some text')
      ->countEachWord()
    ;

    //example to get info for each word
    foreach ($words as $word) {
        printf("%s found %d times", $word->word, $word->count);
    }
    
## Licence

This project has MIT licence. For more information please read LICENCE file.
