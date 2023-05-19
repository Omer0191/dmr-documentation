# My Website

<div class="container">
  <div class="menu">
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
  <div class="content">
    <section id="home">
      <h2>Home</h2>
      <p>Welcome to my website! This is the home page.</p>
    </section>
    
    <section id="about">
      <h2>About</h2>
      <p>This is the about page. Here you can learn more about me and my work.</p>
    </section>
    
    <section id="contact">
      <h2>Contact</h2>
      <p>To get in touch with me, please use the contact information below:</p>
      <ul>
        <li>Email: example@example.com</li>
        <li>Phone: 123-456-7890</li>
      </ul>
    </section>
  </div>
</div>

<style>
.container {
  display: flex;
}

.menu {
  width: 200px;
  background-color: #f2f2f2;
  position: fixed;
  height: 100%;
  overflow: auto;
}

.menu ul {
  list-style-type: none;
  padding: 0;
}

.menu ul li {
  margin: 10px;
}

.content {
  margin-left: 200px;
  padding: 20px;
}
</style>
