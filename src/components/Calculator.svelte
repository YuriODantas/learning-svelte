<script lang="ts">
    import CalculatorModel from "../model/CalculatorModel";
    import Button from "./Button.svelte";
    import Line from "./Line.svelte";
    import Screen from "./Screen.svelte";

    let calc = new CalculatorModel()

    const enteredNumber = (num: string) => calc = calc.enteredNumber(num)
    const operationEntered = (op: string) => calc = calc.operationEntered(op)
    const calculate = () => calc = calc.calculate()
    const pointEntered = () => calc = calc.pointEntered()
    const clear = () => calc = calc.clear()

</script>

<div class="calculator">
  <Screen value={calc.value} />
  <Line>
    <Button highlight triple text="AC" onClick={clear} />
    <Button operation text="/" onClick={operationEntered} />
  </Line>
  <Line>
    <Button text="7" onClick={enteredNumber} />
    <Button text="8" onClick={enteredNumber} />
    <Button text="9" onClick={enteredNumber} />
    <Button operation text="*" onClick={operationEntered} />
  </Line>
  <Line>
    <Button text="4" onClick={enteredNumber} />
    <Button text="5" onClick={enteredNumber} />
    <Button text="6" onClick={enteredNumber} />
    <Button operation text="+" onClick={operationEntered} />
  </Line>
  <Line>
    <Button text="1" onClick={enteredNumber} />
    <Button text="2" onClick={enteredNumber} />
    <Button text="3" onClick={enteredNumber} />
    <Button operation text="-" onClick={operationEntered} />
  </Line>
  <Line>
    <Button double text="0" onClick={enteredNumber} />
    <Button text="," onClick={pointEntered} />
    <Button highlight text="=" onClick={calculate} />
  </Line>
</div>

<style>
  .calculator {
    background-color: var(--background-color);
    height: 220px;
    width: 150px;
    padding: 10px;
    border-radius: 10px;

    display: flex;
    flex-direction: column;
  }
</style>