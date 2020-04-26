## surprise path
  * greet
    - utter_greet
  * surprise {"group":"surprises"}
    - action_retrieve_messages_or_photos
    - utter_anything_else


## message path positive
* greet
    - utter_greet
* messages {"group":"messages"}
    - action_retrieve_messages_or_photos
    - utter_did_you_like_it
* mood_affirm
    - utter_anything_else
* mood_deny
    - utter_goodbye

## message path negative
* greet
    - utter_greet
* messages {"group":"messages"}
    - action_retrieve_messages_or_photos
    - utter_did_you_like_it
* mood_deny
    - utter_sorry_try_again

## photo path positive
  * greet
      - utter_greet
  * photos {"group":"photos"}
      - action_retrieve_messages_or_photos
      - utter_did_you_like_it
  * mood_affirm
      - utter_anything_else
  * mood_deny
      - utter_goodbye

## photo path negative
  * greet
      - utter_greet
  * photos {"group":"photos"}
      - action_retrieve_messages_or_photos
      - utter_did_you_like_it
  * mood_deny
      - utter_sorry_try_again


## fallback story
  * out_of_scope
    - action_default_fallback
