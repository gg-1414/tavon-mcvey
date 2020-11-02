<template>
  <footer>
    <div class="image-block">
      <img src="https://ggclients.s3.amazonaws.com/tavon-mcvey/assets/WCT.gif"/>
    </div>
    <div class="form">
      <h2>Let's Work Together!</h2>
      <form>
        <div class="form-group">
          <label>Name</label>
          <input type="text" name="name" required/>
        </div>
        <div class="form-group">
          <label>Email</label>
          <input type="email" name="email" required />
        </div>
        <div class="form-group">
          <label>Subject</label>
          <input type="text" name="subject" required />
        </div>
        <div class="form-group">
          <label>Message</label>
          <textarea type="text" name="message" required />
        </div>
        <button type="submit">Submit</button>
      </form>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
  footer {
    scroll-snap-align: end;
    display: flex;
    flex-direction: column-reverse;

    .image-block {
      visibility: hidden;
    }

    .form {
      padding: 48px 16px 24px;
      background-color: #eee;

      h2 {
        margin: 20px 0 12px;
      }

      form {
        display: grid;
        gap: 8px;
        text-align: left;
        padding-top: 4px;

        label {
          font-size: 10px;
          font-weight: bold;
          text-transform: uppercase;
          letter-spacing: 1px;
          color: rgb(0 0 0 / 65%);
        }

        input,
        textarea {
          display: block;
          width: 100%;
          padding: 6px;
          margin-top: 4px;
          font-family: monospace;
          font-size: 14px;
        }

        button {
          padding: 6px 12px;
          max-width: 200px;
          margin: 8px auto 0;
          background-color: black;
          color: white;
          border-radius: 4px;
          outline: none;
          border: none;
          cursor: pointer;
          font-size: 14px;
        }
      }
    }
  }
</style>