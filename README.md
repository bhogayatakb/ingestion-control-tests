## Scrape Attributes from Log Body

echo "[2024-12-18T05:27:45.361245] [1] [INFO] Dummy logs message #179" | cat >> scrape-attributes-demo.log

## Multiline Logging

### Sample 1

cat <<EOF >> multiline.log
Exception in thread 1 "prod" java.lang.NullPointerException
at com.example.myproject.Book.getTitle(Book.java:20)
at com.example.myproject.Author.getBookTitles(Author.java:25)
at com.example.myproject.Bootstrap.main(Bootstrap.java:26)
EOF

### Sample 2

cat <<EOF >> multiline-2.log
2025-01-23T19:13:20.508099+0000 INFO: Ignore twilio status callback webhook
of type and scrambled it to make a type specimen book. It has survived not only five centuries, 
but also the leap into electronic typesetting, remaining essentially unchanged. It was 
popularised in the 1960s with the release of Letraset sheets containing Lorem
EOF

### Sample 3

cat <<EOF >> multiline-3.log
2025-01-30T21:22:59.109513+0000 INFO: Saved user with ID 65f35f15cac6470d97baac57, json {"_id": "ObjectId('65f35f15cac6470d97baac57')", "user_phone_number": "+64274493019", "client_info": {"subgroup_config_id": "ObjectId('65c0e94d1eaba01d75bbe721')", "vertical": "taxi", "api_provider": "mtdata", "client": "wellington_combined_taxis", "subgroup": "wellington_combined_taxis"}, "number_of_calls_from_user": 192, "number_of_conversational_calls_from_user": 43, "number_of_callouts_to_user": 3, "custom_attrs": {}, "flow_fields_asked_over_all_calls": {}, "number_of_calls_with_rides_scheduled_through_flip": 31, "cards_on_file": [], "phone_number_type": null} [/var/www/IVR/ivr/metrics/users_and_calls.py:659] <CA29d5c3a75cd9eb9c1448882a8f1a5732, 1738272090.184649.1590682004, taxi, mtdata, wellington_combined_taxis, wellington_combined_taxis, +64274493019, +6448871259, i-00b1a3ad6315258b8-3>
EOF



## JSON Parsing

cat <<EOF >> json-log-processing.log
{"timestamp":"2025-01-23T19:13:20.508099+0000","level":"ERROR","message":"Exception in thread 1 \"prod\" java.lang.NullPointerException","stacktrace":["at com.example.myproject.Book.getTitle(Book.java:20)","at com.example.myproject.Author.getBookTitles(Author.java:25)","at com.example.myproject.Bootstrap.main(Bootstrap.java:26)"]}
EOF