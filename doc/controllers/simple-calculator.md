# Simple Calculator

```java
SimpleCalculatorController simpleCalculatorController = client.getSimpleCalculatorController();
```

## Class Name

`SimpleCalculatorController`


# Calculate

Calculate the expression using specified operation

```java
CompletableFuture<Double> calculateAsync(
    final OperationTypeEnum operation,
    final double x,
    final double y)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `operation` | [`OperationTypeEnum`](../../doc/models/operation-type-enum.md) | Template, Required | operation to perform |
| `x` | `double` | Query, Required | First value |
| `y` | `double` | Query, Required | second value |

## Server

`Server.ENUM_DEFAULT`

## Response Type

`double`

## Example Usage

```java
OperationTypeEnum operation = OperationTypeEnum.MULTIPLY;
double x = 222.14;
double y = 165.14;

simpleCalculatorController.calculateAsync(operation, x, y).thenAccept(result -> {
    // TODO success callback handler
}).exceptionally(exception -> {
    // TODO failure callback handler
    return null;
});
```

