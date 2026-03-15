# Reference
## Health
<details><summary><code>client.health.<a href="src/informly/health/client.py">health_check</a>() -> GetHealthResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the health status of the API service
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
from informly import InformlyClient
from informly.environment import InformlyClientEnvironment

client = InformlyClient(
    token="<token>",
    environment=InformlyClientEnvironment.DEFAULT,
)

client.health.health_check()

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
from informly import InformlyClient
from informly.environment import InformlyClientEnvironment

client = InformlyClient(
    token="<token>",
    environment=InformlyClientEnvironment.DEFAULT,
)

client.contacts.list_contacts()

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

**page:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**page_size:** `typing.Optional[int]` 
    
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
from informly import InformlyClient
from informly.environment import InformlyClientEnvironment

client = InformlyClient(
    token="<token>",
    environment=InformlyClientEnvironment.DEFAULT,
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

**email:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**phone:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**firstname:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**lastname:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**jobtitle:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**company:** `typing.Optional[str]` 
    
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
from informly import InformlyClient
from informly.environment import InformlyClientEnvironment

client = InformlyClient(
    token="<token>",
    environment=InformlyClientEnvironment.DEFAULT,
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

**id:** `str` 
    
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

