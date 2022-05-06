# Roles, Claims and JWT Tokens

## Claims-based authorization

When an identity is created it may be assigned one or more claims issued by a trusted party. A claim is a name value pair that represents what the subject is, not what the subject can do.
Claims based authorization, at its simplest, checks the value of a claim and allows access to a resource based upon that value.

## Claim based authorization checks:

- Are declarative.
- Are applied to Razor Pages, controllers, or actions within a controller.
- Can not be applied at the Razor Page handler level, they must be applied to the Page.

Claims in code specify claims which the current user must possess, and optionally the value the claim must hold to access the requested resource. Claims requirements are policy based, the developer must build and register a policy expressing the claims requirements.

## Add a generic claim check

If the claim value isn't a single value or a transformation is required, use RequireAssertion.

## Multiple Policy Evaluation

If you apply multiple policies to a controller or action, then all policies must pass before access is granted.

## Authentication and Authorization

Authentication is the process of determining who you are, while Authorisation revolves around what you are allowed to do.

## JSON Web Token (JWT)

means of representing claims to be transferred between two parties. The claims in a JWT are encoded as a JSON object that is digitally signed using JSON Web Signature (JWS) and/or encrypted using JSON Web Encryption (JWE).

## JWT Parts

1.  HEADER:

    alg: We have two main algorithms(HS256/RS256) to sign our JWT 3rd part (Signature) which we mention in the headers so that the producer and consumer both should use the same algorithm to verify the token on each end. HS256 indicates that this token is signed using HMAC-SHA256.

    typ: Define the type of the token which is JWT obviously in our case.

2. PAYLOAD: It mostly contains the claims (custom data) and some standard claims as well.

### Standard claims:

- Issuer (iss) - identifies principal that issued the JWT;

- Subject (sub) - identifies the subject of the JWT;

- Audience (aud) - The "aud" (audience) claim identifies the recipients that the JWT is intended for. Each principal intended to process the JWT must identify itself with a value in the audience claim. If the principal processing the claim does not identify itself with a value in the aud claim when this claim is present, then the JWT must be rejected.

- Expiration time (exp) - The "exp" (expiration time) claim identifies the expiration time on or after which the JWT must not be accepted for processing. The value should be in NumericDate format.

- Not before (nbf) - Similarly, the not-before time claim identifies the time on which the JWT will start to be accepted for processing.

- Issued at (iat) - The "iat" (issued at) claim identifies the time at which the JWT was issued.

- JWT ID (jti) - case sensitive unique identifier of the token even among different issuers.

3. SIGNATURE: 

It is calculated by base64url encoding of header and payload and concatenating them with a period as a separator. Then encrypt it with HMAC-SHA256 along with the secret key and the result of the first step.

## Producer and Consumer concept of API’s 

There are two parties involved, one party who gives a service, and the other party who uses the service.

1. Producer is the one who gives a service. It will be the provider(Server) of the API(s) which are JWT protected.

2. Consumer is the one who uses it. It will be the customer(Server/Mobile App/ Web App/ Client) who will be providing the valid JWT token to consume the API(s) being provided by the Producer.
