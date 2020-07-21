## happy path
* greet
  - utter_greet
* mood_great
  - utter_happy
  
## check room and clean now happy path
* greet
  - utter_greet
* book_rooms{"facility_type": "room"}
  - utter_ask_number
* no_of_rooms{"number": "1"}
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
* Restaurant
  - utter_res
* Restaurant_timings
  - utter_restt   
* goodbye
  - utter_goodbye

## story 2
* greet
  - utter_greet
* book_rooms{"facility_type": "room", "number": "1"}
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
* Restaurant
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
* no_of_rooms{"number": "1"}
  - utter_type
* simple_type
  - utter_sd
* deluxe_type
  - utter_dd   
* clean_room{"facility_type1": "clean"}
  - utter_time
* inform{"timing": "one hour"}
  - utter_clean
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
* Restaurant
  - utter_res
* Restaurant_timings
  - utter_restt
* goodbye
  - utter_goodbye  
  
## story 4
* greet
  - utter_greet
* book_rooms{"facility_type": "room", "number": "1"}
  - utter_type
* simple_type
  - utter_sd
* deluxe_type
  - utter_dd 
* clean_room{"facility_type1": "clean"}
  - utter_time
* inform{"timing": "two hours"}
  - utter_clean
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
* Restaurant
  - utter_res
* Restaurant_timings
  - utter_restt   
* goodbye
  - utter_goodbye  

## sad path 1
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* affirm
  - utter_happy

## sad path 2
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* deny
  - utter_goodbye

## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot
