

1. create dart library (mvp)
   - class that manages deck:
     - consists of kanji cards
     - add card to deck
     - delete card from deck
     - card:
       - (all fields from kanji database)
       - kanji
       - activated vocab list (certain words are toggled as active for quizzing)
       - quizzing history
       - time until ready for next quiz
       - readings (likely based on contents of activated vocab list)
       - custom notes
       - quiz functionality:
         - create quiz: return quiz object with selected words to quiz on
         - turn in quiz: give deck manager class information about results (success / fail, tested words, failed attempts, etc.) and update SRS
     - sync contents of deck to Anki
     - save to file (json? yaml?)
     - load from file
   - kanji database from which to add new kanji
     - each kanji contains:
       - kanji
       - name / meaning
       - complete vocab list (all words / phrases in dictionary that contain this kanji)
         - each word tagged with yomichan tags
       - complete radical dropdown list
   - utility like kana romaji -> kana conversion