# Change log

## 1.0.1 (2019-01-29)

* Fixed reliance on `ActionController::Parameters`. Now the strong parameter
  check is only enforced if `ActionController::Parameters` actually exists.

* Fixed missing `require`

* Fixed compatibility with ruby < `2.3.0`

## 1.0.0 (2019-01-23)

* First stable release after being battle-tested over an extended period of
  time.

## Prior to 1.0.0 (beta releases)

### 1.0.0.beta15 (2018-12-11)

* Add method `authorize_called!` to manually mark authorization as called for a
  specific operation.

### 1.0.0.beta14 (2018-11-29)

* Fix bug with jRuby 9.2 where operation class name got mutated when inspecting
  it (see https://github.com/jruby/jruby/issues/5480).

### 1.0.0.beta13 (2018-10-15)

* Explain how to setup load paths in readme

### 1.0.0.beta12 (2018-08-14)

* Exclude param named `escape` from `op_params`.

### 1.0.0.beta11 (2018-07-31)

* Exclude param named `_` from `op_params`. This allows to use `cache: false`
  with `jQuery.ajax`.

### 1.0.0.beta10 (2018-07-18)

* Allow model name override for all models using `RailsOps::ModelMixins`. This
  means you can also specify a model name for models not inheriting from
  `RailsOps::VirtualModel`, i.e.:

  ```ruby
  model User, 'ModelNameOverride'
  ```

### 1.0.0.beta9 (2018-07-04)

* Keep stack trace on exceptions rethrown by `with_rollback_on_exception`.

### 1.0.0.beta8 (2018-05-15)

* Make sure that original state is always restored after calling
  `RailsOps.without_authorization`, even in case of an exception.

### 1.0.0.beta7 (2017-12-19)

* #2 Get rid of protected attributes functionality

### 1.0.0.beta6 (2017-11-27)

* Fix #6 Exceptions in profiler are not re-thrown

### 1.0.0.beta5 (2017-11-27)

* Fix #5 Measure for object_id ... not finished

### 1.0.0.beta4 (2017-11-16)

* Fix a bug where nested models are saved at build time in update operations in
  some cases.

### 1.0.0.beta3 (2017-09-20)

* Fixed log subscription

### 1.0.0.beta2 (2017-09-20)

* Added rubygems badge to readme

* Corrected gem summary

### 1.0.0.beta1 (2017-06-19)

* Initial version as extracted from project

* Start of change log