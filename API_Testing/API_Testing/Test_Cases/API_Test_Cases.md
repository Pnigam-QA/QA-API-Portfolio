# API Test Cases - Hotel Booking

## Base URL: https://restful-booker.herokuapp.com

---

## TC001 - Health Check
| Field | Details |
|-------|---------|
| **Method** | GET |
| **Endpoint** | /ping |
| **Expected Status** | 201 Created |
| **Actual Status** | 201 Created |
| **Result** | ✅ Pass |

---

## TC002 - Generate Auth Token
| Field | Details |
|-------|---------|
| **Method** | POST |
| **Endpoint** | /auth |
| **Request Body** | username, password |
| **Expected Status** | 200 OK |
| **Expected Response** | token value returned |
| **Actual Status** | 200 OK |
| **Result** | ✅ Pass |

---

## TC003 - GET All Bookings
| Field | Details |
|-------|---------|
| **Method** | GET |
| **Endpoint** | /booking |
| **Expected Status** | 200 OK |
| **Expected Response** | List of booking IDs |
| **Actual Status** | 200 OK |
| **Result** | ✅ Pass |

---

## TC004 - CREATE New Booking
| Field | Details |
|-------|---------|
| **Method** | POST |
| **Endpoint** | /booking |
| **Request Body** | firstname, lastname, totalprice, depositpaid, bookingdates, additionalneeds |
| **Expected Status** | 200 OK |
| **Expected Response** | bookingid returned |
| **Actual Status** | 200 OK |
| **Result** | ✅ Pass |

---

## TC005 - UPDATE Booking
| Field | Details |
|-------|---------|
| **Method** | PUT |
| **Endpoint** | /booking/{{booking_id}} |
| **Headers** | Cookie: token={{token}} |
| **Request Body** | Updated totalprice & additionalneeds |
| **Expected Status** | 200 OK |
| **Expected Response** | Updated booking details |
| **Actual Status** | 200 OK |
| **Result** | ✅ Pass |

---

## TC006 - DELETE Booking
| Field | Details |
|-------|---------|
| **Method** | DELETE |
| **Endpoint** | /booking/{{booking_id}} |
| **Headers** | Cookie: token={{token}} |
| **Expected Status** | 201 Created |
| **Expected Response** | Created |
| **Actual Status** | 201 Created |
| **Result** | ✅ Pass |
