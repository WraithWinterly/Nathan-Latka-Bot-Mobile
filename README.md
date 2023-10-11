# Nathan Latka Bot on Mobile: Creating a Real Estate Bot

Looking to create a real estate bot for mobile? There are two approaches to do this: through a **Web Application** or a **Native Application**. Here's a step-by-step breakdown for both:

## Web Application

Streamlit is already mobile-responsive, which implies that your existing application is designed to work seamlessly on a mobile web browser. However, Streamlit cannot be utilized for developing native applications. If your focus is solely on the web platform, you won't not need to transition to another framework.

### Key Points for Web Application:

- Streamlit’s responsiveness allows for mobile browser compatibility without additional modifications.

## Native Application

Developing a native application is feasible through the use of a cross-platform framework like **React Native**. This approach can make the application offer a native feel on both Android and iOS devices.

### Steps for Native Application Development:

1. **API Key Requirement:** Secure your own API key or incorporate a feature allowing users to input their individual keys, akin to the functionality provided by the Streamlit website. Using users own API keys will save us money, but is **very** inconvenient and will result in less usage. A better way would be to bill the users ourselves with pro plans.

2. **Codebase Foundation:** Utilize the LangChain environment as a foundational layer for developing the AI-side. This may require using an external node.js server alongside the application.

3. **Component Building:** Create the application using native components, using APIs from Eleven Labs, LangChain, and Pinecone for the functionality.

### Environment Variables:

- Implement `react-native-dotenv` to manage environment variables within the application.

### UI Conversion:

- Transition from Streamlit UI components to React Native’s distinct component set, including `View`, `Text`, `TextInput`, `Button`, etc.
- For audio playback capabilities, consider using `react-native-sound` or `react-native-track-player`.

### API Calls:

- Utilize the `fetch` method or the Axios library for executing HTTP requests to various services.
- Although API calls to Eleven Labs, OpenAI, and Pinecone maintain consistency in data transmission and reception, the syntax for initiating these calls will differ.

### Data Processing and State Management:

- Reconstruct data processing logic with responses from the services in JavaScript.
- For efficient state management, employ React’s `useState` and `useEffect` hooks, or alternatively, use Redux or zustand.

### Navigation:

- If the application necessitates multiple screens, implement a navigation system with libraries like `react-navigation`. This is best used with a state-management library as well.

## Conclusion

Choosing between a web or native application depends on your specific needs and target audience. For a quick and accessible solution, a web application might suffice. However, for a more robust and responsive user experience, developing a native application is the recommended route.
