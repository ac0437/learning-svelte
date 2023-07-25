<!-- @format -->
<script>
  /**
   * @type {string}
   */
  let firstname;
  /**
   * @type {string}
   */
  let lastname;
  $: fullname = `Hello, ${firstname} ${lastname}`;

  // @ts-ignore
  function setFirstName(event) {
    firstname = event.target.value;
  }

  // @ts-ignore
  function setLastName(event) {
    lastname = event.target.value;
  }
</script>

<input on:change={setFirstName} type="text" placeholder="enter firstname" />
<input on:change={setLastName} type="text" placeholder="enter lastname" />
<span>Your name is: {fullname} </span>
