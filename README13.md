# BloXmove Dev : Vehicle Integration and Management
This page collects architectural options and input for the management and integration of vehicles including related data and services.

## Fleet Gateway
Input provided by Leam
|   |   |
| -----------------------| ------------------------------------------------------------------------ |
| REST API Specification |![This is an image](https://github.com/yatin902/test/blob/main/2335342185/2335342196) |
| Architectural Scheme   |![This is an image](https://github.com/yatin902/test/blob/main/2335342185/2335407723) |

Architecture corresponds to a combination / subset of existing (simulated) Fleet Backend and Virtual Car Wallet components, detailed integration with MBP is not yet defined.

![This is an image](https://github.com/yatin902/test/blob/main/2335342185/2335637100.png)

## Vehicle Onboard Unit Integration
Input provided by Nantis
|   |   |
| -----------------------| ------------------------------------------------------------------------ |
| ![This is an image](https://github.com/yatin902/test/blob/main/2335342185/2335735409) | Concept Document Version 0.2 |

Focusses on integration of physical car wallet based on OLU (On-board Logic Unit) Connect Box.

Suggested approach in two steps: first access / integration via a “Virtual Car Application” (corresponds to Virtual Car Wallet), then direct handling in Physical Car Application

![This is an image](https://github.com/yatin902/test/blob/main/2335342185/2335506027.png)

## Hackathon Prototype With Sodacars
Integration of a real Smart vehicle using the Soda (https://sodacar.com/) Mobility Platform Backend and an xToolTech TBox based on the existing Virtual Car Wallet Architecture and Fleet2Share scenario.

![This is an image](https://github.com/yatin902/test/blob/main/2335342185/2335309423.png)

Code for Virtual Car Wallet Extension allowing flexible Fleet Gateway Adapters, as an example implementing a SodaAdapter accessing a REST API provided by Soda:

https://github.com/bloxmove-com/virtual-car-wallet/blob/master/src/adapters/soda-adapter.class.ts

### Architecture and Requirements for a production-ready Setup
The scenario outlined in the Hackathon can be simplified by controlling both the read access (getting telematics data) and the “write” access (changing state of the car, in our scenario open/close car doors) through the virtual car wallet. This would result in the following basic architecture and requirements for a SODA telematics gateway that can be called by the MBP virtual car wallet component.

![This is an image](https://github.com/yatin902/test/blob/main/2335342185/4446126123.png)

