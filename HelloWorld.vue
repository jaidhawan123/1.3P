<template>
  <div class="hello">
    <h1>WELCOME TO MY CREATION</h1>

    <!-- About Information Box -->
    <div class="about-box">
      <router-link to="/about">
        Well, I'm Jai, 20 years old, studying IT at DEAKIN UNIVERSITY. I'm a person who always seeks to learn new things and enjoys an environment where everything is done in a happy way. This is essentially my resume in which I've shared my personal information. Please read it carefully and consider giving me a chance to become a part of your company as a Team Member.
      </router-link>
    </div>
    
    <router-view></router-view>
    
    <h2>SKILLS</h2>
    <ul>
      <li>Languages:</li>
      <li>Javascript</li>
      <li>HTML</li>
      <li>Vue.js</li>
      <li>Web Designing</li>
    </ul>
    
    <h3>Personal Information</h3>
    <table>
      <thead>
        <tr>
          <th>DATE OF BIRTH</th>
          <th>AGE</th>
          <th>GENDER</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>13-APRIL-2004</td>
          <td>20</td>
          <td>MALE</td>
        </tr>
      </tbody>
    </table>
    
    <h4>AVAILABILITY</h4>
    <table>
      <thead>
        <tr>
          <th>DAYS</th>
          <th>MORNING</th>
          <th>EVENING</th>
          <th>NIGHT</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>MONDAY</td>
          <td>AVAILABLE</td>
          <td>AVAILABLE</td>
          <td>AVAILABLE</td>
        </tr>
        <tr>
          <td>TUESDAY</td>
          <td>AVAILABLE</td>
          <td>AVAILABLE</td>
          <td>AVAILABLE</td>
        </tr>
        <tr>
          <td>WEDNESDAY</td>
          <td>AVAILABLE</td>
          <td>AVAILABLE</td>
          <td>AVAILABLE</td>
        </tr>
        <tr>
          <td>THURSDAY</td>
          <td>AVAILABLE</td>
          <td>AVAILABLE</td>
          <td>AVAILABLE</td>
        </tr>
        <tr>
          <td>FRIDAY</td>
          <td>AVAILABLE</td>
          <td>AVAILABLE</td>
          <td>AVAILABLE</td>
        </tr>
        <tr>
          <td>SATURDAY</td>
          <td>NOT AVAILABLE</td>
          <td>NOT AVAILABLE</td>
          <td>NOT AVAILABLE</td>
        </tr>
        <tr>
          <td>SUNDAY</td>
          <td>NOT AVAILABLE</td>
          <td>NOT AVAILABLE</td>
          <td>NOT AVAILABLE</td>
        </tr>
      </tbody>
    </table>
    
    <div class="form-box">
      <h4>SHARE PERSONAL INFORMATION</h4>
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Name:</label>
          <input type="text" id="name" v-model="formData.name" required>
        </div>
        <div class="form-group">
          <label for="email">Email:</label>
          <input type="email" id="email" v-model="formData.email" required>
        </div>
        <div class="form-group">
          <label for="password">Password:</label>
          <input type="password" id="password" v-model="formData.password" required>
        </div>
        <div class="form-group">
          <label for="requirements">Requirements:</label>
          <input type="text" id="requirements" v-model="formData.requirements" required>
        </div>
        <button type="submit">Submit</button>
      </form>
    </div>

    <!-- Download Resume Link -->
    <a href="https://drive.google.com/file/d/1qucXngPIRe1Hmu4x8EjXTI1t4m6M5-y-/view?usp=drive_link" download="your-resume.pdf" class="resume-link">Download Resume</a>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      formData: {
        name: '',
        email: '',
        password: '',
        requirements: '',
      },
    };
  },
  methods: {
    submitForm() {
      // Handle form submission here
    },
  },
};
</script>

<style scoped>
/* About Box styles */
.about-box {
  background-color: #a477ae; /* Choose your desired background color */
  padding: 20px; /* Adjust the padding as needed */
  border: 2px solid #062d99; /* Border style */
  border-radius: 5px; /* Rounded corners */
  text-align: justify; /* Justify text for a symmetric look */
  margin-bottom: 20px; /* Add some margin to separate it from other content */
}

/* SKILLS list styles */
.SKILLS ul {
  list-style-type: circle;
  padding-left: 1rem;
}
.SKILLS li {
 font-size: medium;
 margin-top: 0.5rem;
}

/* Table styles */
table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 2rem;
  border: 2px solid saddlebrown;
}
table th,
table td {
  padding: 0.5rem;
  text-align: center;
  border: 1px solid seagreen;
}

/* Center-align table header text */
table th {
  text-align: center;
}

/* Form box styles */
.form-box {
  margin-top: 3rem;
  padding: 1rem;
  border: 2px solid #ccc;
  border-radius: 5px;
}

.form-group {
  margin-bottom: 1rem;
}

label {
  display: block;
  font-weight: bold;
}

input[type="text"],
input[type="email"],
input[type="password"] {
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #b10c0c;
  border-radius: 3px;
}

button[type="submit"] {
  background-color: #e576be;
  color: #fff;
  border: none;
  border-radius: 3px;
  padding: 0.5rem 1rem;
  cursor: pointer;
}

/* Resume link styles */
.resume-link {
  display: block;
  margin-top: 1rem;
  color: #007BFF; /* Link color */
  text-decoration: none;
}
</style>
