

# ListCarriers200ResponseDataInnerConfigValue

## anyOf schemas
* [BigDecimal](BigDecimal.md)
* [Boolean](Boolean.md)
* [String](String.md)

## Example
```java
// Import classes:
import com.zippendo.sdk.model.ListCarriers200ResponseDataInnerConfigValue;
import com.zippendo.sdk.model.BigDecimal;
import com.zippendo.sdk.model.Boolean;
import com.zippendo.sdk.model.String;

public class Example {
    public static void main(String[] args) {
        ListCarriers200ResponseDataInnerConfigValue exampleListCarriers200ResponseDataInnerConfigValue = new ListCarriers200ResponseDataInnerConfigValue();

        // create a new BigDecimal
        BigDecimal exampleBigDecimal = new BigDecimal();
        // set ListCarriers200ResponseDataInnerConfigValue to BigDecimal
        exampleListCarriers200ResponseDataInnerConfigValue.setActualInstance(exampleBigDecimal);
        // to get back the BigDecimal set earlier
        BigDecimal testBigDecimal = (BigDecimal) exampleListCarriers200ResponseDataInnerConfigValue.getActualInstance();

        // create a new Boolean
        Boolean exampleBoolean = new Boolean();
        // set ListCarriers200ResponseDataInnerConfigValue to Boolean
        exampleListCarriers200ResponseDataInnerConfigValue.setActualInstance(exampleBoolean);
        // to get back the Boolean set earlier
        Boolean testBoolean = (Boolean) exampleListCarriers200ResponseDataInnerConfigValue.getActualInstance();

        // create a new String
        String exampleString = new String();
        // set ListCarriers200ResponseDataInnerConfigValue to String
        exampleListCarriers200ResponseDataInnerConfigValue.setActualInstance(exampleString);
        // to get back the String set earlier
        String testString = (String) exampleListCarriers200ResponseDataInnerConfigValue.getActualInstance();
    }
}
```


