- if circuit breaker does not trip automatically then any fault can be fatal. that's why trip circuit supervision is required.
- TCS relay monitor everything.
- TCS relay inject small current(3 mA) in tripping circuit and get's back to the relay. if it is healthy then same amount of current gets back to relay, otherwise if current is not same amount of sender then TCS will send alarm to the circuit breaker.
- if tripping coil in tripping circuit is not energized then TCS will send alarm. if tripping coil is open or not energized then it is abnormality.
- if tripping coil is supply missing then it is also sensed by TCS relay and generates alarm. also auxiliary supply.
- TCS relay working is divided in two methods: 
1. Pre monitoring: when Circuit breaker is in off condition in this condition also TCS relay works.
2. Post monitoring: when circuit breaker is on condition then also TCS relay wokrs.