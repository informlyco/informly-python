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

**email:** `typing.Optional[str]` — Email address of the contact
    
</dd>
</dl>

<dl>
<dd>

**phone:** `typing.Optional[str]` — Phone number of the contact
    
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

**company:** `typing.Optional[str]` — Company of contact (if different) or organization name
    
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

