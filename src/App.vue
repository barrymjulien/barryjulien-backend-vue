<template>
  <div>
    <b-container fluid class="header">
      <b-row>
        <b-col cols="12" class="header">
          <h1>BarryJulien.com</h1>
        </b-col>
      </b-row>
    </b-container>

    <b-container fluid class="profile">
  <b-row>
    <b-col cols="12" md="6" lg="3" class="profile-column-1 text-center">
      <img src="https://source.unsplash.com/c_GmwfHBDzk/200x200" alt="Profile Picture">
    </b-col>
    <b-col cols="12" md="6" lg="9" class="profile-column-2">
      <h2>Barry Julien</h2>
      <p>Software Engineer</p>
    </b-col>
  </b-row>
</b-container>

    <b-container fluid class="blog">
       <b-row>
        <b-col cols="12">
          <h2>Blog</h2>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="4" v-for="post in blog" :key="post">
          <b-card :title="post.title" :img-src="post.image" img-alt="Image" img-top>
            <b-card-text>
              {{ post.description }}
            </b-card-text>
          </b-card>
        </b-col>
      </b-row>
    </b-container>

    <b-container fluid class="contact">
      <b-row>
        <b-col cols="12">
          <h2>Get in Touch</h2>
        </b-col>
      </b-row>
      <b-row>
        <b-col lg="6">
          <b-form>
            <b-form-group id="input-group-1" label="Name:" label-for="input-1">
              <b-form-input id="input-1" type="text" required placeholder="Enter name"></b-form-input>
            </b-form-group>
            <b-form-group id="input-group-2" label="Email address:" label-for="input-2">
              <b-form-input id="input-2" type="email" required placeholder="Enter email"></b-form-input>
            </b-form-group>
            <b-button type="submit" variant="primary">Submit</b-button>
          </b-form>
        </b-col>
      </b-row>
    </b-container>

    <b-container fluid class="footer">
      <b-row>
        <b-col cols="12" class="text-center">
          <p>&copy; 2023 BarryJulien.com</p>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      portfolio: [
        { title: 'Project 1', image: 'https://source.unsplash.com/c_GmwfHBDzk/200x200', description: 'This is project 1' },
        { title: 'Project 2', image: 'https://source.unsplash.com/c_GmwfHBDzk/200x200', description: 'This is project 2' },
        { title: 'Project 3', image: 'https://source.unsplash.com/c_GmwfHBDzk/200x200', description: 'This is project 3' }
      ],
      blog: [
        { title: 'Post 1', image: 'https://source.unsplash.com/c_GmwfHBDzk/200x200', description: 'This is post 1' },
        { title: 'Post 2', image: 'https://source.unsplash.com/c_GmwfHBDzk/200x200', description: 'This is post 2' },
        { title: 'Post 3', image: 'https://source.unsplash.com/c_GmwfHBDzk/200x200', description: 'This is post 3' }
      ]
    }
  }
}
</script>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

.header {
  background-color: #333;
  color: #fff;
  padding: 1rem;
}

.profile {
  background-color: #e71d3f;
  padding: 2rem;
}

.profile-column-1 {
  background-color: #c61399;
  padding: 20px;
}

.profile-column-2 {
  background-color: #e6d753;
  padding: 20px;
}

.portfolio {
  background-color: #4CAF50;
  padding: 2rem;
}

.blog {
  background-color: #2196F3;
  padding: 2rem;
}

.contact {
  background-color: #ff9800;
  padding: 2rem;
}

.footer {
  background-color: #333;
  color: #fff;
  padding: 1rem;
  text-align: center;
  clear: both;
}
</style>