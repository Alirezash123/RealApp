 Task exception was never retrieved
future: <Task finished name='Task-9' coro=<UpdateMethods._dispatch_update() done, defined at /usr/local/lib/python3.12/site-packages/telethon/client/updates.py:521> exception=UsernameInvalidError('Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\\w\\d]{3,30}[a-zA-Z\\d]" (caused by ResolveUsernameRequest)')>
Traceback (most recent call last):
  File "/usr/local/lib/python3.12/site-packages/telethon/client/updates.py", line 561, in _dispatch_update
    await builder.resolve(self)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 99, in resolve
    await self._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/newmessage.py", line 93, in _resolve
    await super()._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 103, in _resolve
    self.chats = await _into_id_set(client, self.chats)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 33, in _into_id_set
    chat = await client.get_input_entity(chat)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 445, in get_input_entity
    await self._get_entity_from_string(peer))
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 561, in _get_entity_from_string
    result = await self(
             ^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 30, in __call__
    return await self._call(self._sender, request, ordered=ordered)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 92, in _call
    result = await future
             ^^^^^^^^^^^^
telethon.errors.rpcerrorlist.UsernameInvalidError: Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\w\d]{3,30}[a-zA-Z\d]" (caused by ResolveUsernameRequest)
2025-05-03 20:37:43,684 - ERROR - Task exception was never retrieved
future: <Task finished name='Task-10' coro=<UpdateMethods._dispatch_update() done, defined at /usr/local/lib/python3.12/site-packages/telethon/client/updates.py:521> exception=UsernameInvalidError('Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\\w\\d]{3,30}[a-zA-Z\\d]" (caused by ResolveUsernameRequest)')>
Traceback (most recent call last):
  File "/usr/local/lib/python3.12/site-packages/telethon/client/updates.py", line 561, in _dispatch_update
    await builder.resolve(self)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 99, in resolve
    await self._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/newmessage.py", line 93, in _resolve
    await super()._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 103, in _resolve
    self.chats = await _into_id_set(client, self.chats)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 33, in _into_id_set
    chat = await client.get_input_entity(chat)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 445, in get_input_entity
    await self._get_entity_from_string(peer))
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 561, in _get_entity_from_string
    result = await self(
             ^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 30, in __call__
    return await self._call(self._sender, request, ordered=ordered)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 92, in _call
    result = await future
             ^^^^^^^^^^^^
telethon.errors.rpcerrorlist.UsernameInvalidError: Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\w\d]{3,30}[a-zA-Z\d]" (caused by ResolveUsernameRequest)
2025-05-03 20:37:43,708 - ERROR - Task exception was never retrieved
future: <Task finished name='Task-11' coro=<UpdateMethods._dispatch_update() done, defined at /usr/local/lib/python3.12/site-packages/telethon/client/updates.py:521> exception=UsernameInvalidError('Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\\w\\d]{3,30}[a-zA-Z\\d]" (caused by ResolveUsernameRequest)')>
Traceback (most recent call last):
  File "/usr/local/lib/python3.12/site-packages/telethon/client/updates.py", line 561, in _dispatch_update
    await builder.resolve(self)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 99, in resolve
    await self._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/newmessage.py", line 93, in _resolve
    await super()._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 103, in _resolve
    self.chats = await _into_id_set(client, self.chats)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 33, in _into_id_set
    chat = await client.get_input_entity(chat)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 445, in get_input_entity
    await self._get_entity_from_string(peer))
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 561, in _get_entity_from_string
    result = await self(
             ^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 30, in __call__
    return await self._call(self._sender, request, ordered=ordered)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 92, in _call
    result = await future
             ^^^^^^^^^^^^
telethon.errors.rpcerrorlist.UsernameInvalidError: Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\w\d]{3,30}[a-zA-Z\d]" (caused by ResolveUsernameRequest)
2025-05-03 20:37:43,732 - ERROR - Task exception was never retrieved
future: <Task finished name='Task-12' coro=<UpdateMethods._dispatch_update() done, defined at /usr/local/lib/python3.12/site-packages/telethon/client/updates.py:521> exception=UsernameInvalidError('Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\\w\\d]{3,30}[a-zA-Z\\d]" (caused by ResolveUsernameRequest)')>
Traceback (most recent call last):
  File "/usr/local/lib/python3.12/site-packages/telethon/client/updates.py", line 561, in _dispatch_update
    await builder.resolve(self)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 99, in resolve
    await self._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/newmessage.py", line 93, in _resolve
    await super()._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 103, in _resolve
    self.chats = await _into_id_set(client, self.chats)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 33, in _into_id_set
    chat = await client.get_input_entity(chat)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 445, in get_input_entity
    await self._get_entity_from_string(peer))
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 561, in _get_entity_from_string
    result = await self(
             ^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 30, in __call__
    return await self._call(self._sender, request, ordered=ordered)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 92, in _call
    result = await future
             ^^^^^^^^^^^^
telethon.errors.rpcerrorlist.UsernameInvalidError: Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\w\d]{3,30}[a-zA-Z\d]" (caused by ResolveUsernameRequest)
2025-05-03 20:37:43,760 - ERROR - Task exception was never retrieved
future: <Task finished name='Task-13' coro=<UpdateMethods._dispatch_update() done, defined at /usr/local/lib/python3.12/site-packages/telethon/client/updates.py:521> exception=UsernameInvalidError('Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\\w\\d]{3,30}[a-zA-Z\\d]" (caused by ResolveUsernameRequest)')>
Traceback (most recent call last):
  File "/usr/local/lib/python3.12/site-packages/telethon/client/updates.py", line 561, in _dispatch_update
    await builder.resolve(self)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 99, in resolve
    await self._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/newmessage.py", line 93, in _resolve
    await super()._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 103, in _resolve
    self.chats = await _into_id_set(client, self.chats)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 33, in _into_id_set
    chat = await client.get_input_entity(chat)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 445, in get_input_entity
    await self._get_entity_from_string(peer))
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 561, in _get_entity_from_string
    result = await self(
             ^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 30, in __call__
    return await self._call(self._sender, request, ordered=ordered)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/client/users.py", line 92, in _call
    result = await future
             ^^^^^^^^^^^^
telethon.errors.rpcerrorlist.UsernameInvalidError: Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\w\d]{3,30}[a-zA-Z\d]" (caused by ResolveUsernameRequest)
2025-05-03 20:37:43,786 - ERROR - Task exception was never retrieved
future: <Task finished name='Task-14' coro=<UpdateMethods._dispatch_update() done, defined at /usr/local/lib/python3.12/site-packages/telethon/client/updates.py:521> exception=UsernameInvalidError('Nobody is using this username, or the username is unacceptable. If the latter, it must match r"[a-zA-Z][\\w\\d]{3,30}[a-zA-Z\\d]" (caused by ResolveUsernameRequest)')>
Traceback (most recent call last):
  File "/usr/local/lib/python3.12/site-packages/telethon/client/updates.py", line 561, in _dispatch_update
    await builder.resolve(self)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 99, in resolve
    await self._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/newmessage.py", line 93, in _resolve
    await super()._resolve(client)
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 103, in _resolve
    self.chats = await _into_id_set(client, self.chats)
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/usr/local/lib/python3.12/site-packages/telethon/events/common.py", line 33, in _into_id_set
    chat = await client.get_input_entity(chat)
