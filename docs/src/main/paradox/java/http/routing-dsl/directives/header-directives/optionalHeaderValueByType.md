<a id="optionalheadervaluebytype-java"></a>
# optionalHeaderValueByType

## Description

Optionally extracts the value of the HTTP request header of the given type.

The `optionalHeaderValueByType` directive is similar to the @ref[headerValueByType](headerValueByType.md#headervaluebytype-java) directive but always extracts
an `Optional` value instead of rejecting the request if no matching header could be found.

@@@ note

Custom headers will only be matched by this directive if they extend `ModeledCustomHeader`
from the Scala DSL and there is currently no API for the Java DSL (Ticket #20415)

To learn more about defining custom headers, read: @ref[Custom Headers](../../../common/http-model.md#custom-headers-scala).

@@@

## Example

@@snip [HeaderDirectivesExamplesTest.java](../../../../../../../test/java/docs/http/javadsl/server/directives/HeaderDirectivesExamplesTest.java) { #optionalHeaderValueByType }