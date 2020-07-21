#### This file contains tests to evaluate that your bot behaves as expected.
#### If you want to learn more, please see the docs: https://rasa.com/docs/rasa/user-guide/testing-your-assistant/

## happy path 1
* greet: hello there!
  - utter_greet
* mood_great: amazing
  - utter_happy

## happy path 2
* greet: hello there!
  - utter_greet
* mood_great: amazing
  - utter_happy
* goodbye: bye-bye!
  - utter_goodbye
  
## check room and clean now happy path
* greet
  - utter_greet
* book_rooms{"facility_type": "room"}
  - utter_ask_number
* no_of_rooms{"number": "one"}
  - utter_type
* simple_type
  - utter_sd
* deluxe_type
  - utter_dd 
* clean_room{"facility_type1": "clean"}
  - utter_time
* now
  - utter_schedule  
* faq_check_in
  - utter_checkin
* faq_checkout  
  - utter_checkout
* faq_breakfast_availability
  - utter_bfa
* faq_breakfasttime
  - utter_bft
* faq_cancel_reservation     
  - utter_cr
* faq_cancellationpolicy
  - utter_cp  
* restaurant
  - utter_res
* Restaurant_timings
  - utter_restt   
* goodbye
  - utter_goodbye

## story 2
* greet
  - utter_greet
* book_rooms{"facility_type": "room", "number": "one"}
  - utter_type
* simple_type
  - utter_sd
* deluxe_type
  - utter_dd 
* clean_room{"facility_type1": "clean"}
  - utter_time
* now
  - utter_schedule  
* faq_check_in
  - utter_checkin
* faq_checkout  
  - utter_checkout
* faq_breakfast_availability
  - utter_bfa
* faq_breakfasttime
  - utter_bft
* faq_cancel_reservation     
  - utter_cr
* faq_cancellationpolicy
  - utter_cp  
* restaurant
  - utter_res
* Restaurant_timings
  - utter_restt   
* goodbye
  - utter_goodbye 
  
## check room + room cleaning time happy path
 * greet
  - utter_greet
* book_rooms{"facility_type": "room"}
  - utter_ask_number
* no_of_rooms{"number": "one"}
  - utter_type
* simple_type
  - utter_sd
* deluxe_type
  - utter_dd   
* clean_room{"facility_type1": "clean"}
  - utter_time
* inform{"timing": "hours"}
  - action_clean
* faq_check_in
  - utter_checkin
* faq_checkout  
  - utter_checkout
* faq_breakfast_availability
  - utter_bfa
* faq_breakfasttime
  - utter_bft
* faq_cancel_reservation     
  - utter_cr
* faq_cancellationpolicy
  - utter_cp  
* restaurant
  - utter_res
* Restaurant_timings
  - utter_re  
* goodbye
  - utter_goodbye  
  
## story 4
* greet
  - utter_greet
* book_rooms{"facility_type": "room"}
  - utter_ask_number
* no_of_rooms{"number": "one"}
  - utter_type
* simple_type
  - utter_sd
* deluxe_type
  - utter_dd 
* clean_room{"facility_type1": "clean"}
  - utter_time
* inform{"timing": "hours"}
  - action_clean
* faq_check_in
  - utter_checkin
* faq_checkout  
  - utter_checkout
* faq_breakfast_availability
  - utter_bfa
* faq_breakfasttime
  - utter_bft
* faq_cancel_reservation     
  - utter_cr
* faq_cancellationpolicy
  - utter_cp  
* restaurant
  - utter_res
* Restaurant_timings
  - utter_restt   
* goodbye
  - utter_goodbye  
  

## sad path 1
* greet: hello
  - utter_greet
* mood_unhappy: not good
  - utter_cheer_up
  - utter_did_that_help
* affirm: yes
  - utter_happy

## sad path 2
* greet: hello
  - utter_greet
* mood_unhappy: not good
  - utter_cheer_up
  - utter_did_that_help
* deny: not really
  - utter_goodbye

## sad path 3
* greet: hi
  - utter_greet
* mood_unhappy: very terrible
  - utter_cheer_up
  - utter_did_that_help
* deny: no
  - utter_goodbye

## say goodbye
* goodbye: bye-bye!
  - utter_goodbye

## bot challenge
* bot_challenge: are you a bot?
  - utter_iamabot
