# Change Log

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

<a name="0.10.0"></a>
# [0.10.0](https://github.com/an-sh/chat-service/compare/v0.9.2...v0.10.0) (2016-08-22)


### Bug Fixes

* don't use deprecated Buffer api on newer node ([6d4f5b4](https://github.com/an-sh/chat-service/commit/6d4f5b4))
* **api:** remove notifications on duplicate joins ([c1c2cd2](https://github.com/an-sh/chat-service/commit/c1c2cd2))


### BREAKING CHANGES

* api: Store api UserState#addSocketToRoom method must return
now two values.



<a name="0.9.2"></a>
## [0.9.2](https://github.com/an-sh/chat-service/compare/v0.9.1...v0.9.2) (2016-08-16)


### Bug Fixes

* add disconnection errors logging ([289eda5](https://github.com/an-sh/chat-service/commit/289eda5))



<a name="0.9.1"></a>
## [0.9.1](https://github.com/an-sh/chat-service/compare/v0.9.0...v0.9.1) (2016-08-12)


### Bug Fixes

* **docs:** examples build-in reconnection handling ([28ff554](https://github.com/an-sh/chat-service/commit/28ff554))



<a name="0.9.0"></a>
# [0.9.0](https://github.com/an-sh/chat-service/compare/0.8.0...v0.9.0) (2016-08-08)


### Bug Fixes

* **api:** add internal errors representation ([6984215](https://github.com/an-sh/chat-service/commit/6984215))
* **api:** don't send notifications on noop leaves ([0d05357](https://github.com/an-sh/chat-service/commit/0d05357))
* **api:** don't transform exec command results ([33d753c](https://github.com/an-sh/chat-service/commit/33d753c))
* **config:** honor enableUserlistUpdates option ([86f5f61](https://github.com/an-sh/chat-service/commit/86f5f61))
* **store:** trim history on shrinking ([826b59a](https://github.com/an-sh/chat-service/commit/826b59a))
* **transport:** use ioOptions with http ([8d93755](https://github.com/an-sh/chat-service/commit/8d93755))


### Code Refactoring

* remove io and nps fields ([6b28fde](https://github.com/an-sh/chat-service/commit/6b28fde))
* remove redis field ([7e14b62](https://github.com/an-sh/chat-service/commit/7e14b62))
* **api:** rename defaultHistoryLimit option ([a3ae131](https://github.com/an-sh/chat-service/commit/a3ae131))
* **errors:** new rpc error object format ([7c34202](https://github.com/an-sh/chat-service/commit/7c34202))
* **transport:** move middleware option ([7f839f5](https://github.com/an-sh/chat-service/commit/7f839f5))
* **validation:** provide a method on instance ([5ed60a9](https://github.com/an-sh/chat-service/commit/5ed60a9))


### Features

* **api:** add a custom data field to ExecInfo ([be5bb48](https://github.com/an-sh/chat-service/commit/be5bb48))
* **api:** add getHandshakeData transport method ([8d3c089](https://github.com/an-sh/chat-service/commit/8d3c089))
* **api:** add notification config setters methods ([bf6935c](https://github.com/an-sh/chat-service/commit/bf6935c))
* **api:** add roomNotificationsInfo command ([e1a7ac5](https://github.com/an-sh/chat-service/commit/e1a7ac5))
* **api:** echo join and leave from a server side ([23d2252](https://github.com/an-sh/chat-service/commit/23d2252))
* **api:** per-room notifications config ([c21435b](https://github.com/an-sh/chat-service/commit/c21435b))
* **hooks:** add isLocalCall property ([37b2260](https://github.com/an-sh/chat-service/commit/37b2260))
* **hooks:** add onDisconnect hook ([e9ff9a1](https://github.com/an-sh/chat-service/commit/e9ff9a1))
* **store:** permissions lists size limits ([5aa917a](https://github.com/an-sh/chat-service/commit/5aa917a))
* **store:** pluginable state store ([408f785](https://github.com/an-sh/chat-service/commit/408f785))
* **transport:** transport as a plugin ([892bacb](https://github.com/an-sh/chat-service/commit/892bacb))


### Styles

* rewrite all code to es6 ([f47173f](https://github.com/an-sh/chat-service/commit/f47173f))


### BREAKING CHANGES

* api: Rename defaultHistoryLimit option to historyMaxSize.
* api: enableAccessListsUpdates and enableUserlistUpdates are
now just default values, and will not be used for already created rooms.
* Remove ChatService redis field from the public API.
* Remove ChatService io and nps fields from the public
API.
* Possible regressions due to a full es6 rewrite.
* transport: Multiple transport API changes.
* hooks: Remove disconnect command and its hooks.
* transport: Option middleware was moved from hooks to
SocketIOTransportOptions.
* errors: The ChatService errors' object name field is set to
'ChatServiceError' and name filed is renamed to code.
* validation: chatService.validator.checkArguments has changed to
chatService.checkArguments.
