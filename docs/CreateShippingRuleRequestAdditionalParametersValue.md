

# CreateShippingRuleRequestAdditionalParametersValue

## anyOf schemas
* [BigDecimal](BigDecimal.md)
* [Boolean](Boolean.md)
* [CreateShippingRuleRequestAdditionalParametersValueAnyOf](CreateShippingRuleRequestAdditionalParametersValueAnyOf.md)
* [String](String.md)

## Example
```java
// Import classes:
import com.zippendo.sdk.model.CreateShippingRuleRequestAdditionalParametersValue;
import com.zippendo.sdk.model.BigDecimal;
import com.zippendo.sdk.model.Boolean;
import com.zippendo.sdk.model.CreateShippingRuleRequestAdditionalParametersValueAnyOf;
import com.zippendo.sdk.model.String;

public class Example {
    public static void main(String[] args) {
        CreateShippingRuleRequestAdditionalParametersValue exampleCreateShippingRuleRequestAdditionalParametersValue = new CreateShippingRuleRequestAdditionalParametersValue();

        // create a new BigDecimal
        BigDecimal exampleBigDecimal = new BigDecimal();
        // set CreateShippingRuleRequestAdditionalParametersValue to BigDecimal
        exampleCreateShippingRuleRequestAdditionalParametersValue.setActualInstance(exampleBigDecimal);
        // to get back the BigDecimal set earlier
        BigDecimal testBigDecimal = (BigDecimal) exampleCreateShippingRuleRequestAdditionalParametersValue.getActualInstance();

        // create a new Boolean
        Boolean exampleBoolean = new Boolean();
        // set CreateShippingRuleRequestAdditionalParametersValue to Boolean
        exampleCreateShippingRuleRequestAdditionalParametersValue.setActualInstance(exampleBoolean);
        // to get back the Boolean set earlier
        Boolean testBoolean = (Boolean) exampleCreateShippingRuleRequestAdditionalParametersValue.getActualInstance();

        // create a new CreateShippingRuleRequestAdditionalParametersValueAnyOf
        CreateShippingRuleRequestAdditionalParametersValueAnyOf exampleCreateShippingRuleRequestAdditionalParametersValueAnyOf = new CreateShippingRuleRequestAdditionalParametersValueAnyOf();
        // set CreateShippingRuleRequestAdditionalParametersValue to CreateShippingRuleRequestAdditionalParametersValueAnyOf
        exampleCreateShippingRuleRequestAdditionalParametersValue.setActualInstance(exampleCreateShippingRuleRequestAdditionalParametersValueAnyOf);
        // to get back the CreateShippingRuleRequestAdditionalParametersValueAnyOf set earlier
        CreateShippingRuleRequestAdditionalParametersValueAnyOf testCreateShippingRuleRequestAdditionalParametersValueAnyOf = (CreateShippingRuleRequestAdditionalParametersValueAnyOf) exampleCreateShippingRuleRequestAdditionalParametersValue.getActualInstance();

        // create a new String
        String exampleString = new String();
        // set CreateShippingRuleRequestAdditionalParametersValue to String
        exampleCreateShippingRuleRequestAdditionalParametersValue.setActualInstance(exampleString);
        // to get back the String set earlier
        String testString = (String) exampleCreateShippingRuleRequestAdditionalParametersValue.getActualInstance();
    }
}
```


