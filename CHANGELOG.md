0.7
----------------

* Now Pupil supporting Twitter API 1.1.

0.6.2
----------------

* 一部API 1.1に対応

0.6.1
----------------

* エラーの際にfalseを返さない不具合を修正

0.6
----------------

* New method: Pupil#followers, Pupil#friends
* Some bug fixed

0.4.1
----------------

* Eyedrops v1.0 released!

0.4.0
----------------

* Added new commandline tool.
  "Eyedrops, the interactive Pupil"
* Pupil::Keygen are supported readline.

0.3.3
----------------

* Jeweler to Bundler gem

0.3.2
----------------

* Fixed minor issue.

0.3.1
----------------

* Fixed bugs in Pupil::Stream#follow

0.3.0
----------------

* Unknown resistance function are supported.<br />
  If called method is not implemented, Pupil recognize API endpoint by method name and tries access to unknown API automatically.<br />
  e.g. pupil.account_totals => GET /1/account/totals.json
* Stream::Hash support

0.2.2
----------------

* New method Pupil#timeline is the some as Pupil#home_timeline
* New method Pupil#timeline_for is the some as Pupil#user_timeline
* Not necessary to give @screen_name parameter when Pupil.new . It is now on optionally parameter.
* Pupil#followers_ids and Pupil#friends_ids returns Array of ids

0.2.1
----------------

* Some bug fixed.

0.2.0
----------------

* Fixed bug that :include(and :exclude) parameter had not worked.
* New form are supported.<br/>
  Classic form:<br/>
	`pupil = Pupil.new(…)`<br/>
    `pupil.destroy(status_id) #=> Delete tweet`<br/>
  New one:<br/>
	`status = timeline.first`<br/>
	`status.destroy`
* Mutable scheme are supported. When Twitter REST API is changed, Schemes correspond to it automatically.
* New ways to distinguish screen_name from user_id.
  If methods catch parameter of number, recognize it as user_id.
* Almost Lists API are supported.

0.1.5
----------------

* Pupil::Stream Error handling(Pupil::Stream::StreamError) are rejected.


0.1.4
----------------

* Rename Search stream method, :filter to :search
* Search REST API are supported
* Pupil::Stream::Shash is outdated. Instead, use Pupil::Stream::Hash
* New class, Pupil::Stream::Array
* Pupil#public_timeline are supported

0.1.3
----------------

* Fixed a bug that Pupil::Stream::Status has not user variable

0.1.2
----------------

* Added new classes,
Pupil::Stream::Status and Pupil::Stream::Shash
* Pupil::Stream#start returned only Pupil::Stream::Status or Pupil::Stream::Shash
* They have "event" variable that show type of event uniformly

0.1.1
----------------

* First release