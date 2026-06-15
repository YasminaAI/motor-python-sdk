# Reference
## Quotes
<details><summary><code>client.quotes.<a href="src/yasminaai/quotes/client.py">show_quote</a>(...) -> QuoteResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from yasminaai import YasminaaiApi
from yasminaai.environment import YasminaaiApiEnvironment

client = YasminaaiApi(
    token="<token>",
    environment=YasminaaiApiEnvironment.DEFAULT,
)

client.quotes.show_quote(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.quotes.<a href="src/yasminaai/quotes/client.py">delete_quote</a>(...) -> DeleteQuoteRequestsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from yasminaai import YasminaaiApi
from yasminaai.environment import YasminaaiApiEnvironment

client = YasminaaiApi(
    token="<token>",
    environment=YasminaaiApiEnvironment.DEFAULT,
)

client.quotes.delete_quote(
    id=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `int` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.quotes.<a href="src/yasminaai/quotes/client.py">list_quotes</a>() -> GetQuoteRequestsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from yasminaai import YasminaaiApi
from yasminaai.environment import YasminaaiApiEnvironment

client = YasminaaiApi(
    token="<token>",
    environment=YasminaaiApiEnvironment.DEFAULT,
)

client.quotes.list_quotes()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.quotes.<a href="src/yasminaai/quotes/client.py">request_quotes</a>(...) -> QuoteResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

For getting prices with benefits. 
The Quote IDs can be used later to issue a policy
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from yasminaai import YasminaaiApi
from yasminaai.environment import YasminaaiApiEnvironment
import datetime

client = YasminaaiApi(
    token="<token>",
    environment=YasminaaiApiEnvironment.DEFAULT,
)

client.quotes.request_quotes(
    owner_id="owner_id",
    phone="phone",
    birthdate=datetime.date.fromisoformat("2023-01-15"),
    car_sequence_number="car_sequence_number",
    car_estimated_cost=1.1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**owner_id:** `str` — Owner ID must be 10 digits starting with 1, 2, or 7
    
</dd>
</dl>

<dl>
<dd>

**phone:** `str` — Phone number must start with 05 and be 10 digits
    
</dd>
</dl>

<dl>
<dd>

**birthdate:** `datetime.date` — Birthdate in YYYY-MM-DD format
    
</dd>
</dl>

<dl>
<dd>

**car_sequence_number:** `str` — Car sequence number must be 8 or 9 digits
    
</dd>
</dl>

<dl>
<dd>

**car_estimated_cost:** `float` — Estimated cost of the car
    
</dd>
</dl>

<dl>
<dd>

**email:** `typing.Optional[str]` — Email address must be valid and belongs to the customer
    
</dd>
</dl>

<dl>
<dd>

**is_ownership_transfer:** `typing.Optional[bool]` — Indicates if the ownership is being transferred
    
</dd>
</dl>

<dl>
<dd>

**current_car_owner_id:** `typing.Optional[str]` — Required if is_ownership_transfer is true; 10 digits starting with 1,2,7
    
</dd>
</dl>

<dl>
<dd>

**car_model_year:** `typing.Optional[int]` — Car model year between 1950 and next year
    
</dd>
</dl>

<dl>
<dd>

**start_date:** `typing.Optional[datetime.date]` — Desired policy start date in YYYY-MM-DD. Must be between tomorrow and 28 days from today (inclusive). The platform validates this range server-side.
    
</dd>
</dl>

<dl>
<dd>

**drivers:** `typing.Optional[typing.List[PostQuoteRequestsRequestDriversItem]]` — List of drivers for the vehicle. When provided, the sum of all driving_percentage values must equal 100, and the owner must be included among the drivers.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Policies
<details><summary><code>client.policies.<a href="src/yasminaai/policies/client.py">show_policy</a>(...) -> Policy</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Show a specific policy
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from yasminaai import YasminaaiApi
from yasminaai.environment import YasminaaiApiEnvironment

client = YasminaaiApi(
    token="<token>",
    environment=YasminaaiApiEnvironment.DEFAULT,
)

client.policies.show_policy(
    car_policy=1,
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**car_policy:** `int` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.policies.<a href="src/yasminaai/policies/client.py">list_policies</a>(...) -> typing.List[Policy]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Listing requested policies
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from yasminaai import YasminaaiApi
from yasminaai.environment import YasminaaiApiEnvironment

client = YasminaaiApi(
    token="<token>",
    environment=YasminaaiApiEnvironment.DEFAULT,
)

client.policies.list_policies()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**quote_request_id:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**quote_price_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**provider_policy_id:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**car_sequence_number:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**new_owner_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**previous_owner_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**min_price:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**max_price:** `typing.Optional[float]` 
    
</dd>
</dl>

<dl>
<dd>

**per_page:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.policies.<a href="src/yasminaai/policies/client.py">issue_policy</a>(...) -> Policy</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

For issuing a new policy
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from yasminaai import YasminaaiApi
from yasminaai.environment import YasminaaiApiEnvironment

client = YasminaaiApi(
    token="<token>",
    environment=YasminaaiApiEnvironment.DEFAULT,
)

client.policies.issue_policy(
    quote_request_id=123,
    quote_reference_id="550e8400-e29b-41d4-a716-446655440000",
    quote_price_id="550e8400-e29b-41d4-a716-446655440001",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**quote_request_id:** `int` — ID of the car quote request
    
</dd>
</dl>

<dl>
<dd>

**quote_reference_id:** `str` — Unique identifier for the quote reference ID (coming from POST /quote-requests)
    
</dd>
</dl>

<dl>
<dd>

**quote_price_id:** `str` — Unique identifier for the quote price ID that exists inside a quote item (coming from POST /quote-requests)
    
</dd>
</dl>

<dl>
<dd>

**benefits:** `typing.Optional[typing.List[str]]` — List of benefit UUIDs
    
</dd>
</dl>

<dl>
<dd>

**extra_fields:** `typing.Optional[typing.Dict[str, typing.Any]]` — Optional free-form object with additional fields. Total JSON-encoded size must not exceed 255 characters.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## OtPs
<details><summary><code>client.ot_ps.<a href="src/yasminaai/ot_ps/client.py">request_otp_for_quote_verification</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint sends a one-time password (OTP) to the provided email and phone number for quote verification. It should be called before creating a quote request.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from yasminaai import YasminaaiApi
from yasminaai.environment import YasminaaiApiEnvironment

client = YasminaaiApi(
    token="<token>",
    environment=YasminaaiApiEnvironment.DEFAULT,
)

client.ot_ps.request_otp_for_quote_verification(
    email="someone@example.com",
    phone="0501234567",
    owner_id="1012345678",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**email:** `str` — Email address of the car owner
    
</dd>
</dl>

<dl>
<dd>

**phone:** `str` — Phone number starting with 05 and containing 10 digits
    
</dd>
</dl>

<dl>
<dd>

**owner_id:** `str` — National ID or Iqama ID of the car owner (10 digits)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ot_ps.<a href="src/yasminaai/ot_ps/client.py">request_otp_for_issuing_policy</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

This endpoint sends a one-time password (OTP). It should be called before issuing a policy.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from yasminaai import YasminaaiApi
from yasminaai.environment import YasminaaiApiEnvironment

client = YasminaaiApi(
    token="<token>",
    environment=YasminaaiApiEnvironment.DEFAULT,
)

client.ot_ps.request_otp_for_issuing_policy(
    email="someone@example.com",
    phone="0501234567",
    owner_id="1012345678",
    quote_request_id=123,
    quote_reference_id="550e8400-e29b-41d4-a716-446655440000",
    quote_price_id="550e8400-e29b-41d4-a716-446655440001",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**email:** `str` — Email address of the car owner
    
</dd>
</dl>

<dl>
<dd>

**phone:** `str` — Phone number starting with 05 and containing 10 digits
    
</dd>
</dl>

<dl>
<dd>

**owner_id:** `str` — National ID or Iqama ID of the car owner (10 digits)
    
</dd>
</dl>

<dl>
<dd>

**quote_request_id:** `int` — ID of the car quote request
    
</dd>
</dl>

<dl>
<dd>

**quote_reference_id:** `str` — Unique identifier for the quote reference ID (coming from POST /quote-requests)
    
</dd>
</dl>

<dl>
<dd>

**quote_price_id:** `str` — Unique identifier for the quote price ID that exists inside a quote item (coming from POST /quote-requests)
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

