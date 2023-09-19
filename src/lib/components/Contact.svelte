<script>
    let name = "";
    let email = "";
    let message = "";
  
    function handleSubmit() {
      console.log("Nom:", name);
      console.log("Email:", email);
      console.log("Message:", message);
  
      name = "";
      email = "";
      message = "";
    }
  </script>
  
  <main style="background-color: #f4f4f4; min-height: 100vh; display: flex; justify-content: center; align-items: center;">
    <div style="font-family: 'Montserrat', sans-serif; background-color: white; padding: 20px; border-radius: 10px; box-shadow: 0px 0px 10px lightgray ; width: 100%; max-width: 400px;">
      <h1 style="font-size: 24px; font-weight: bold; margin-bottom: 20px;">Contactez-nous</h1>
      <form on:submit|preventDefault={handleSubmit}>
        <div style="margin-bottom: 10px;">
          <label for="name" style="display: block; font-size: 14px; font-weight: bold; margin-bottom: 5px;">Nom</label>
          <input type="text" id="name" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px;" bind:value={name} required />
        </div>
        <div style="margin-bottom: 10px;">
          <label for="email" style="display: block; font-size: 14px; font-weight: bold; margin-bottom: 5px;">Email</label>
          <input type="email" id="email" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px;" bind:value={email} required />
        </div>
        <div style="margin-bottom: 10px;">
          <label for="message" style="display: block; font-size: 14px; font-weight: bold; margin-bottom: 5px;">Message</label>
          <textarea id="message" style="width: 100%; padding: 10px; border: 1px solid #ccc; border-radius: 4px;" bind:value={message} rows="4" required></textarea>
        </div>
        <div style="text-align: center;">
          <button type="submit" style="background-color: #007bff; color: white; padding: 10px 20px; font-weight: bold; border: none; border-radius: 4px; cursor: pointer; transition: background-color 0.3s;">Envoyer</button>
        </div>
      </form>
    </div>
  </main>
  