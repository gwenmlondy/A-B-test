# A-B-test
The relaunching of an A/B test for an international online store

### Project Purpose

The relaunching of an A/B test  for an international online store

**The Technical description left from the previous test:**

- Test name: `recommender_system_test`
- Groups: А (control), B (new payment funnel)
- Launch date: 2020-12-07
- Date when they stopped taking up new users: 2020-12-21
- End date: 2021-01-01
- Audience: 15% of the new users from the EU region
- Purpose of the test: testing changes related to the introduction of an improved recommendation system
- Expected result: within 14 days of signing up, users will show better conversion into product page views (the `product_page` event), instances of adding items to the shopping cart (`product_cart`), and purchases (`purchase`). At each stage of the funnel `product_page → product_cart → purchase`, there will be at least a 10% increase.
- Expected number of test participants: 6000


### Data Description
    
#### Structure of ab_project__marketing_events_us.csv:

The marketing events dataset (`ab_project__marketing_events_us.csv`) has the following structure:

- `name`: The name of the marketing event
- `regions`: Regions where the ad campaign will be held
- `start_dt`: Campaign start date
- `finish_dt`: Campaign end date    
    
#### Structure of final_ab_new_users_upd_us.csv:

The `final_ab_new_users_upd_us.csv` file has the following structure:

- `user_id`
- `first_date`: Sign-up date
- `region`
- `device`: Device used to sign up

#### Structure of final_ab_events_upd_us.csv:

The `final_ab_events_upd_us.csv` file has the following structure:

- `user_id`
- `event_dt`: Event date and time
- `event_name`: Event type name
- `details`: Additional data on the event (e.g., order total in USD for purchase events)

#### Structure of final_ab_participants_upd_us.csv:

The `final_ab_participants_upd_us.csv` file has the following structure:

- `user_id`
- `ab_test`: Test name
- `group`: The test group the user belonged to    
