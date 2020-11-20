<template>
  <footer>
    <div class="image-block">
      <img src="https://ggclients.s3.amazonaws.com/tavon-mcvey/assets/WCT.gif"/>
    </div>
    <div class="form-block">
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
    scroll-snap-align: start;
    display: flex;
    flex-direction: column-reverse;

    .image-block {
      visibility: hidden;
    }

    .form-block {
      padding: 48px 16px 24px;
      background-color: #eee;

      h2 {
        margin: 20px 0 12px;
      }

      form {
        display: grid;
        text-align: left;
        padding-top: 4px;
        max-width: 640px;
        margin: auto;

        .form-group {
          margin-bottom: 8px;
        }

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
          font-family: inherit;
          font-size: 14px;
        }
      }
    }
  }

  @media screen and (min-width: 768px) {
    footer {
      .form-block {
        h2 {
          margin-bottom: 16px;
          margin-top: 32px;
        }

        form {
          .form-group {
            margin-bottom: 16px;
          }

          label {
            font-size: 14px;
          }

          input,
          textarea {
            padding: 12px 16px;
            font-size: 16px;
            margin-top: 12px;
          }
        }
      }
    }
  }
</style>