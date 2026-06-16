<script setup>
import { ref } from 'vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import StudentProfile from './components/StudentProfile.vue'
import StatsSection from './components/StatsSection.vue'
import CourseInfo from './components/CourseInfo.vue'
import AssignmentList from './components/AssignmentList.vue'
import ActivityTimeline from './components/ActivityTimeline.vue'
import ProductCard from './components/ProductCard.vue'
// Create Student Data
const student = {
  avatar: 'https://placehold.co/150',
  fullName: 'Alex Morgan',
  email: 'alex.m@edu.com',
  batch: '2026-A',
  track: 'Frontend Development'
}
//Create Stats Data
const stats = [
  {
    title: 'Lessons Completed',
    value: '12/20',
    icon: '📚'
  },
  {
    title: 'Exercises Done',
    value: '8/10',
    icon: '✏️'
  },
  {
    title: 'Current Score',
    value: '92%',
    icon: '🏆'
  },
  {
    title: 'Attendance Rate',
    value: '95%',
    icon: '📅'
  }
]
// Create Course Data
const course = {
  courseName: "Frontend Frameworks (Vue 3)",
  instructor: "Prof. Evans",
  progress: 60
}
// Create Assignments Data
const assignments = [
  {
    title: "Composition API Quiz",
    dueDate: "June 15",
    status: "Completed"
  },
  {
    title: "Props Lab Exercise",
    dueDate: "June 15",
    status: "Pending"
  }
]
// Create Activities Data 
const activities = [
  {
    activityName: "Submitted Exercise",
    date: "2 mins ago",
    type: "submit"
  },
  {
    activityName: "Quiz Completed",
    date: "1 hour ago",
    type: "quiz"
  }
]
//create product data
const products = [
  {
    name: 'Laptop',
    price: 800,
    inStock: true
  },
  {
    name: 'Keyboard',
    price: 50,
    inStock: true
  },
  {
    name: 'Mouse',
    price: 25,
    inStock: false
  }
]
// create cart item state
const cart = ref([])
// add to cart function
function handleAddToCart(productName) {
  cart.value.push(productName)
}

</script>

<template>
  <Header />

  <h1>Vue Props Practice Lab</h1>

  // add student profile
  <StudentProfile :avatar="student.avatar" :fullName="student.fullName" :email="student.email" :batch="student.batch"
    :track="student.track" />
  <!-- Student Profile -->
  <StudentProfile />

  //add course info
  <CourseInfo :courseName="course.courseName" :instructor="course.instructor" :progress="course.progress" />
  //add assignment list
  <AssignmentList :assignments="assignments" />
  //add activity timeline
  <ActivityTimeline :activities="activities" />


<!-- Product Practice Section -->

<h2>Product Practice Section</h2>

<ProductCard
  v-for="product in products"
  :key="product.name"
  :name="product.name"
  :price="product.price"
  :inStock="product.inStock"
  @addedToCart="handleAddToCart"
/>

<h3>Shopping Cart</h3>

<ul>
  <li
    v-for="item in cart"
    :key="item"
  >
    {{ item }}
  </li>
</ul>

  <Footer />
</template>