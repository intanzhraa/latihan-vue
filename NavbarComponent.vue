<script setup>
import { Navbar, NavbarLogo, NavbarCollapse, NavbarLink } from 'flowbite-vue'
</script>
<template>
    <Navbar>
      <template #logo>
        <NavbarLogo link="https://www.google.com/" alt="Flowbite logo" image-url="https://s-light.tiket.photos/t/01E25EBZS3W0FY9GTG6C42E1SE/rsfit1920640gsm/events/2022/06/07/920d815c-3aa0-4d6a-9761-32ea90435b8f-1654612950188-e46999327aef777c61c9d574943d3508.png">
          JKT48 
        </NavbarLogo>
      </template>
      <template #default="{isShowMenu}">
        <NavbarCollapse :isShowMenu="isShowMenu">
          <NavbarLink isActive link="#">HOME</NavbarLink>
          <NavbarLink link="#">MEMBER</NavbarLink>
          <NavbarLink link="#">SHOP</NavbarLink>
          <NavbarLink link="#">THEATER</NavbarLink>
        </NavbarCollapse>
      </template>
    </Navbar>
</template>
