<template>
    <div class="main-content">
      <breadcumb :page="'User Manager'" :folder="'Users'" :folder2="'User Manager'" />
     
    </div>
  </template>
  
 
  <style>
  ul.gull-pagination li {
    margin: 0 12px;
  }
  
  ul.gull-pagination li .page-link {
    border-radius: 50% !important;
    border-color: #fff !important;
  }
  .page-link:hover {
    background-color: #fff;
  }
  .page-link:focus {
    box-shadow: 0 0 0 0.2rem rgb(255, 255, 255);
  }
  .page-item.disabled .page-link {
    color: #d5d0d9;
  }
  
  .list-enter-active,
  .list-leave-active,
  .list-move {
    transition: 500ms cubic-bezier(0.59, 0.12, 0.34, 0.95);
    transition-property: opacity, transform;
  }
  
  .list-enter {
    opacity: 0;
    transform: translateX(50px) scaleY(0.5);
  }
  
  .list-enter-to {
    opacity: 1;
    transform: translateX(0) scaleY(1);
  }
  
  .list-leave-active {
    position: absolute;
  }
  
  .list-leave-to {
    opacity: 0;
    transform: scaleY(0);
    transform-origin: center top;
  }
  .fade-transition {
    opacity: 1;
  }
  .fade-enter-active,
  .fade-leave-active {
    transition: all 0.5s ease-in-out;
  }
  
  .fade-enter,
  .fade-leave-active {
    transform: translate(100%);
    opacity: 0;
  }
  </style>
  