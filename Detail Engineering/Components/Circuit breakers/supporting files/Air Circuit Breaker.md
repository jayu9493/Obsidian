---
tags:
  - Supportingfiles
related:
  - industry
  - Electrical
created: 2024-08-25
---
---
## Basic Introduction:
### Currents definition:
- ***Icu*** : **Breaking capacity** the maximum fault-current a circuit-breaker can successfully interrupt without being damaged.
- ***Ics*** : **rated service short-circuit breaking capacity** a specific test sequence that includes the circuit breaker's ability to carry 85% of its nontripping current for a certain amount of time.
IEC 60947-2 expresses Ics as a percentage of Icu, with values of 25%, 50%, 75%, and 100% for industrial circuit breakers. For domestic circuit breakers, Ics = k Icn.
- ***Icw*** :   **rated short-time withstand current** a value that indicates how much current a circuit breaker can withstand for a given amount of time without being damaged.
- *Icm*:  
- Air circuit breaker have LSIG settings to set which depends on the **nominal current** of the breaker. 
- They are normally used at LT side in industry and because of it's compact size it is industry's favourite for using in panel.
- ACB comes in 800A to 10,000 A.  
- ---
### Catalogues:
- We use this circuit breakers in industry:
		1. L&T omega breaker
		2. L&T CN & CS  
		3. siemens breakers ( old MVSB and lagoon)
- Catalogue: [[OMEGA_ACB_Manual_2.3.pdf]]
- Catalogue: [[C-Power_ACB_Catalogue_1.7.pdf]]
---
## Construction and components:

### Construction:
- [[ACB.excalidraw]]
- There are Three relays in ACB.
### Main Components Of ACB:
1. ***Shunt Release coil*:** Remotely ACB trip also for various faults it is used. 
	- The primary function of a shunt coil is to allow remote control or automated systems to trip the circuit breaker. This means that if a fault condition or a specific control signal is detected, the coil receives a voltage that energizes the coil, causing the breaker to trip.
	- The UVR provides protection against undervoltage conditions, but the shunt coil does not monitor system voltage. Instead, it requires an external signal to trip the breaker.
2. **Under voltage release coil:** only breaker close when undervoltage coil is energized.
3. **close release coil**: breaker's closing from remote and mechanical and electrical interlocking should be provided.
4. **spring charging motor:** to charge the spring.
5. **arc chutes**: to distinguish the arc.
6. **anti-pumping relay**:It is a circuit breaker auxiliary relay that is used to protect the circuit breaker from multiple closing commands.
7. **Protection and control unit**: for doing necessary settings in breakers.
8. **Jaw contacts**: They are flexible contacts which contact points between breaker and busbar.
9. **Control wiring circuits**: They are upper side of breaker normally and have 
### Omega ACB components:

| ![[Pasted image 20240930215439.png]] | ![[Pasted image 20240930215443.png]] | ![[Pasted image 20240930215623.png \| center \| 600]] |
| :----------------------------------: | :----------------------------------: | :---------------------------------------------------: |
#### SIC (Secondary isolating contacts):
#### Arc shield:

#### Wiring for breakers:

