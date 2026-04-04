# Reference
## Contacts
<details><summary><code>client.contacts.<a href="src/informly/contacts/client.py">list_contacts</a>(...) -> ListContactsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from informly import Informly
from informly.environment import InformlyEnvironment

client = Informly(
    token="<token>",
    environment=InformlyEnvironment.DEFAULT,
)

client.contacts.list_contacts(
    page=1,
    page_size=20,
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

**page:** `typing.Optional[int]` — Page number (1-indexed)
    
</dd>
</dl>

<dl>
<dd>

**page_size:** `typing.Optional[int]` — Number of items per page (1-100)
    
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

<details><summary><code>client.contacts.<a href="src/informly/contacts/client.py">create_contact</a>(...) -> CreateContactResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Creates a new contact or updates an existing one if a contact with the same email or phone already exists. Optionally assigns segments and redeems a referral code.
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
from informly import Informly
from informly.environment import InformlyEnvironment

client = Informly(
    token="<token>",
    environment=InformlyEnvironment.DEFAULT,
)

client.contacts.create_contact()

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

**email:** `typing.Optional[str]` — Email address. Required if phone is not provided.
    
</dd>
</dl>

<dl>
<dd>

**phone:** `typing.Optional[str]` — Phone number in E.164 format. Required if email is not provided.
    
</dd>
</dl>

<dl>
<dd>

**firstname:** `typing.Optional[str]` — First name of the contact
    
</dd>
</dl>

<dl>
<dd>

**lastname:** `typing.Optional[str]` — Last name of the contact
    
</dd>
</dl>

<dl>
<dd>

**jobtitle:** `typing.Optional[str]` — Job title of the contact
    
</dd>
</dl>

<dl>
<dd>

**company:** `typing.Optional[str]` — Company or organization name
    
</dd>
</dl>

<dl>
<dd>

**segment_ids:** `typing.Optional[typing.List[str]]` — Segment IDs to assign to the contact
    
</dd>
</dl>

<dl>
<dd>

**referral_code:** `typing.Optional[str]` — Referral code to redeem for this contact
    
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

<details><summary><code>client.contacts.<a href="src/informly/contacts/client.py">delete_contacts</a>(...) -> DeleteContactsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from informly import Informly
from informly.environment import InformlyEnvironment

client = Informly(
    token="<token>",
    environment=InformlyEnvironment.DEFAULT,
)

client.contacts.delete_contacts(
    ids=[
        "ids"
    ],
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

**ids:** `typing.List[str]` — Contact IDs to delete
    
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

<details><summary><code>client.contacts.<a href="src/informly/contacts/client.py">get_contact</a>(...) -> GetContactResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from informly import Informly
from informly.environment import InformlyEnvironment

client = Informly(
    token="<token>",
    environment=InformlyEnvironment.DEFAULT,
)

client.contacts.get_contact(
    id="id",
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

**id:** `str` — Unique identifier of the resource
    
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

<details><summary><code>client.contacts.<a href="src/informly/contacts/client.py">update_contact</a>(...) -> UpdateContactResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Updates an existing contact's fields. If segmentIds is provided, it replaces all existing segment assignments.
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
from informly import Informly
from informly.environment import InformlyEnvironment

client = Informly(
    token="<token>",
    environment=InformlyEnvironment.DEFAULT,
)

client.contacts.update_contact(
    id="id",
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

**id:** `str` — Unique identifier of the resource
    
</dd>
</dl>

<dl>
<dd>

**email:** `typing.Optional[str]` — Email address of the contact
    
</dd>
</dl>

<dl>
<dd>

**phone:** `typing.Optional[str]` — Phone number in E.164 format (e.g. +14155552671)
    
</dd>
</dl>

<dl>
<dd>

**firstname:** `typing.Optional[str]` — First name of the contact
    
</dd>
</dl>

<dl>
<dd>

**lastname:** `typing.Optional[str]` — Last name of the contact
    
</dd>
</dl>

<dl>
<dd>

**jobtitle:** `typing.Optional[str]` — Job title of the contact
    
</dd>
</dl>

<dl>
<dd>

**company:** `typing.Optional[str]` — Company or organization name
    
</dd>
</dl>

<dl>
<dd>

**segment_ids:** `typing.Optional[typing.List[str]]` — Segment IDs to assign (replaces existing segments)
    
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

<details><summary><code>client.contacts.<a href="src/informly/contacts/client.py">delete_contact</a>(...) -> DeleteContactResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from informly import Informly
from informly.environment import InformlyEnvironment

client = Informly(
    token="<token>",
    environment=InformlyEnvironment.DEFAULT,
)

client.contacts.delete_contact(
    id="id",
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

**id:** `str` — Unique identifier of the resource
    
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

## Segments
<details><summary><code>client.segments.<a href="src/informly/segments/client.py">list_segments</a>() -> ListSegmentsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns all segments available in the organization.
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
from informly import Informly
from informly.environment import InformlyEnvironment

client = Informly(
    token="<token>",
    environment=InformlyEnvironment.DEFAULT,
)

client.segments.list_segments()

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

