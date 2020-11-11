<script>
  import { elements } from '../Data/PeriodicTableJSON.json';
  export let style;
  export let atomicNumber;
  const toCamelCase = (input) => {
    let regex = /\s+(\w)?/gi;
    let output = input.toLowerCase().replace(regex, function (match, letter) {
      return letter.toUpperCase();
    });
    return output;
  };
</script>

<style>
  .element {
    height: 4.8vw;
    width: 4.8vw;
    background-color: #cbd5e0;
    border-collapse: collapse;
  }
  .element-atomic-number {
    font-size: 0.7vw;
  }
  .element-symbol {
    font-size: 1.2vw;
    margin-bottom: -0.1rem;
  }
  .element-name {
    font-size: 0.65vw;
  }
  /* Category Colors */
  .diatomicNonmetal {
    background-color: #faf089;
  }
  .nobleGas {
    background-color: #fbd38d;
  }
  .alkaliMetal {
    background-color: #feb2b2;
  }
  .alkalineEarthMetal {
    background-color: #7f9cf5;
  }
  .metalloid {
    background-color: #90cdf4;
  }
  .polyatomicNonmetal {
    background-color: #81e6d9;
  }
  .transitionMetal {
    background-color: #9ae6b4;
  }
  .post-transitionMetal {
    background-color: #9ae6b4;
  }
  .lanthanide {
    background-color: #fbb6ce;
  }
  .actinide {
    background-color: #d6bcfa;
  }
</style>

<button
  type="button"
  class=" element p-1 rounded shadow-xl cursor-pointer overflow-hidden border {toCamelCase(elements[atomicNumber - 1].category)}"
  {style}>
  <div>
    <div class="-mb-1 font-light text-left element-atomic-number">
      {atomicNumber}
    </div>
    <div>
      <h3 class="mx-auto font-semibold text-center element-symbol">
        {elements[atomicNumber - 1].symbol}
      </h3>
    </div>
    <div class="mx-auto overflow-hidden font-light text-center element-name">
      {elements[atomicNumber - 1].name}
    </div>
    <div class="mx-auto overflow-hidden font-light text-center element-name" />
  </div>
</button>
