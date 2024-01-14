<template>
<div id="menu">
    <div id="title">
        <svg width="32" height="33" viewBox="0 0 32 33" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M28 16.4998L12 16.4998M28 8.49984L12 8.49984M28 24.4998L12 24.4998M6.66667 16.4998C6.66667 17.2362 6.06971 17.8332 5.33333 17.8332C4.59695 17.8332 4 17.2362 4 16.4998C4 15.7635 4.59695 15.1665 5.33333 15.1665C6.06971 15.1665 6.66667 15.7635 6.66667 16.4998ZM6.66667 8.49984C6.66667 9.23622 6.06971 9.83317 5.33333 9.83317C4.59695 9.83317 4 9.23622 4 8.49984C4 7.76346 4.59695 7.1665 5.33333 7.1665C6.06971 7.1665 6.66667 7.76346 6.66667 8.49984ZM6.66667 24.4998C6.66667 25.2362 6.06971 25.8332 5.33333 25.8332C4.59695 25.8332 4 25.2362 4 24.4998C4 23.7635 4.59695 23.1665 5.33333 23.1665C6.06971 23.1665 6.66667 23.7635 6.66667 24.4998Z" stroke="#3B3B3B" stroke-width="2.66667" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
        <h2>To-do List</h2>
    </div>
    <div id="menuOptions">
        <button class="buttonMenu">All</button>
        <button class="buttonMenu">Done</button>
        <button class="buttonMenu">Undone</button>
    </div>
</div>
</template>

<script>


</script>

<style>
#title {
    display: flex;
    align-items: center;
    vertical-align: middle;
    gap: 10px;
    color: #7A7A7A;
}

#title h2 {
    font-size: 18px;
}

#menu {
    display: flex;
    justify-content: center; /*centralizar*/
    align-items: center; /*centralizar*/
    vertical-align: middle; /*alinhar horizontal*/
    gap: 15%;
    width: 600px;
}

#menuOptions {
    display: flex;
    gap: 6px;
}

.buttonMenu {
    cursor: pointer;
    padding: 8px 24px;
    border-radius: 15px;
    background: #292929;
    border: transparent;
    color: #7A7A7A;
    font-weight: 600;
    font-size: 18px;
}

.buttonMenu:hover {
    background: #E63E21;
    color: #F7E3D9;
}
</style>