<div class="footer">
    <div class="footer-nav">
        <a href="#">About Us</a>
        <a href="#">Services</a>
        <a href="#">Case Studies</a>
        <a href="#">Contact</a>
        <a href="#">Careers</a>
    </div>
    <div class="social-links">
        <a href="#"><i class="fab fa-twitter"></i></a>
        <a href="#"><i class="fab fa-linkedin"></i></a>
        <a href="#"><i class="fab fa-github"></i></a>
        <a href="#"><i class="fab fa-instagram"></i></a>
    </div>
</div>

<style>
    .footer {
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-top: 1px solid rgba(255, 255, 255, 0.1);
        padding-top: 2rem;
        margin-top: 2rem;
    }
    
    .footer-nav {
        display: flex;
        gap: 2rem;
    }
    
    .footer a {
        color: var(--light-gray);
        text-decoration: none;
        transition: all 0.3s ease;
        font-weight: 500;
        position: relative;
    }
    
    .footer a:hover {
        color: var(--primary);
    }
    
    .footer a::after {
        content: '';
        position: absolute;
        bottom: -2px;
        left: 0;
        width: 0;
        height: 2px;
        background: var(--primary);
        transition: width 0.3s ease;
    }
    
    .footer a:hover::after {
        width: 100%;
    }
    
    .social-links {
        display: flex;
        gap: 1.5rem;
    }
    
    .social-links a {
        color: var(--light-gray);
        opacity: 0.7;
        transition: all 0.3s ease;
    }
    
    .social-links a:hover {
        opacity: 1;
        color: var(--primary);
        transform: translateY(-2px);
    }

    @media (max-width: 768px) {
        .footer {
            flex-direction: column;
            gap: 1.5rem;
            text-align: center;
        }
        
        .footer-nav {
            flex-direction: column;
            gap: 1rem;
        }
    }
</style>