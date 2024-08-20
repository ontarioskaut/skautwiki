---
title: Minihra Skautská historie
description: 
published: true
date: 2024-08-20T10:56:26.531Z
tags: 
editor: markdown
dateCreated: 2024-08-20T10:47:24.924Z
---

# Minihra Skautská historie

<div class="minigame">
  <div class="container_wrapper">
        <div class="container_start">
            <p class="draggable" draggable="true" data-order="10">1</p>
            <p class="draggable" draggable="true" data-order="20">2</p>
            <p class="draggable" draggable="true" data-order="30">3</p>
            <p class="draggable" draggable="true" data-order="40">4</p>
        </div>
        <div class="container_final"></div>
    </div>
    <div class="button_wrapper">
        <button id="checking-btn">Check order</button>
    </div>
    <p id="result"></p>
  </div>
    <script>
        const draggables = document.querySelectorAll('.draggable');
        const containers = document.querySelectorAll('.container_start, .container_final');

        draggables.forEach(draggable => {
            draggable.addEventListener('dragstart', () => {
                draggable.classList.add('dragging');
                document.querySelector('.container_final').style.backgroundColor = '#444';
                document.getElementById('result').textContent = "";
            });

            draggable.addEventListener('dragend', () => {
                draggable.classList.remove('dragging');
            });
        });

        containers.forEach(container => {
            container.addEventListener('dragover', e => {
                e.preventDefault();
                const afterElement = getDragAfterElement(container, e.clientY);
                const draggable = document.querySelector('.dragging');
                if (afterElement == null) {
                    container.appendChild(draggable);
                } else {
                    container.insertBefore(draggable, afterElement);
                }
            });
        });

        function getDragAfterElement(container, y) {
            const draggableElements = [...container.querySelectorAll('.draggable:not(.dragging)')];

            return draggableElements.reduce((closest, child) => {
                const box = child.getBoundingClientRect();
                const offset = y - box.top - box.height / 2;
                if (offset < 0 && offset > closest.offset) {
                    return { offset: offset, element: child };
                } else {
                    return closest;
                }
            }, { offset: Number.NEGATIVE_INFINITY }).element;
        }

        document.getElementById('checking-btn').addEventListener('click', checkOrder);

        function checkOrder() {
            const array = Array.from(document.querySelectorAll('.container_final .draggable'));
            const orderArray = array.map(eve => Number(eve.getAttribute('data-order')));
            const isSorted = orderArray.every((value, index) => {
                return index == 0 || value >= orderArray[index - 1];
            });

            if (isSorted) {
                document.getElementById('result').textContent = "Correct";
                document.querySelector('.container_final').style.backgroundColor = 'green';
            } else {
                document.getElementById('result').textContent = "Incorrect";
                document.querySelector('.container_final').style.backgroundColor = 'red';
            }
        }
    </script>