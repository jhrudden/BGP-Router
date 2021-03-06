# CS3700 Project 3

### Dean Frame, John Henry Rudden

## Implementation

We utilized the Python starter code provided to us, since it helped us break the project down into individual functions that we needed to complete. To hold data received from update messages, we used a Route class. Then, in the Router class, we keyed each port to a list of Routes that our router had received on those ports. This became what we used as our forwarding table. For dump messages, we formatted the data in each route to adhere to the table message specfications. For data packets, we simplify determined which Routes led to the destination address by comparing a Routes network to the data address anded to a subnet mask. We then found the path that was most favoriable by passing it through several rounds of filtering, before we sent packets on their way.

For aggregation, we created a separate unaggregated table. We used this table to aggregate whenever our list of routes was updated. For disaggregation, we aggregate as normal except we don't add any routes to the aggregated table that have been revoked.

## Challenges

One of the main challenges we ran into was using Python. We both used Golang for previous class projects, but since the starter code is in Python we decided to make the switch. While we both had used Python for previous classes, we found ourselves frequently running into syntax errors and looking up the specifics of Python's libraries. However, we still believe that it was worth it to use Python, since the starter code was very well organized and made the project much more clear.

Another challenge that we faced was the aggregation of routes. It took us some time to understand the aggregation process and, more specifically, what adjacency meant. We were able to pass the 6-1 and 6-2 test cases.

## Testing

For testing, we used the provided tests to ensure that our router was operating correctly. We also used many print statements when we wanted to know more about how our router worked and any problems that the router might be running into.
