

# ListShippingRules200ResponseDataInnerAdditionalParametersValue

## anyOf schemas
* [BigDecimal](BigDecimal.md)
* [Boolean](Boolean.md)
* [ListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf](ListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf.md)
* [String](String.md)

## Example
```java
// Import classes:
import com.zippendo.sdk.model.ListShippingRules200ResponseDataInnerAdditionalParametersValue;
import com.zippendo.sdk.model.BigDecimal;
import com.zippendo.sdk.model.Boolean;
import com.zippendo.sdk.model.ListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf;
import com.zippendo.sdk.model.String;

public class Example {
    public static void main(String[] args) {
        ListShippingRules200ResponseDataInnerAdditionalParametersValue exampleListShippingRules200ResponseDataInnerAdditionalParametersValue = new ListShippingRules200ResponseDataInnerAdditionalParametersValue();

        // create a new BigDecimal
        BigDecimal exampleBigDecimal = new BigDecimal();
        // set ListShippingRules200ResponseDataInnerAdditionalParametersValue to BigDecimal
        exampleListShippingRules200ResponseDataInnerAdditionalParametersValue.setActualInstance(exampleBigDecimal);
        // to get back the BigDecimal set earlier
        BigDecimal testBigDecimal = (BigDecimal) exampleListShippingRules200ResponseDataInnerAdditionalParametersValue.getActualInstance();

        // create a new Boolean
        Boolean exampleBoolean = new Boolean();
        // set ListShippingRules200ResponseDataInnerAdditionalParametersValue to Boolean
        exampleListShippingRules200ResponseDataInnerAdditionalParametersValue.setActualInstance(exampleBoolean);
        // to get back the Boolean set earlier
        Boolean testBoolean = (Boolean) exampleListShippingRules200ResponseDataInnerAdditionalParametersValue.getActualInstance();

        // create a new ListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf
        ListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf exampleListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf = new ListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf();
        // set ListShippingRules200ResponseDataInnerAdditionalParametersValue to ListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf
        exampleListShippingRules200ResponseDataInnerAdditionalParametersValue.setActualInstance(exampleListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf);
        // to get back the ListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf set earlier
        ListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf testListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf = (ListShippingRules200ResponseDataInnerAdditionalParametersValueAnyOf) exampleListShippingRules200ResponseDataInnerAdditionalParametersValue.getActualInstance();

        // create a new String
        String exampleString = new String();
        // set ListShippingRules200ResponseDataInnerAdditionalParametersValue to String
        exampleListShippingRules200ResponseDataInnerAdditionalParametersValue.setActualInstance(exampleString);
        // to get back the String set earlier
        String testString = (String) exampleListShippingRules200ResponseDataInnerAdditionalParametersValue.getActualInstance();
    }
}
```


