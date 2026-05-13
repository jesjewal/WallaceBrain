# Instructional Design Evaluation and Automated Quality Assessment: A Briefing Document

## Executive Summary

The evaluation of instructional design (ID) has evolved from subjective aesthetic reviews to a rigorous, data-driven discipline centered on procedural integrity, pedagogical alignment, and measurable performance impact. Current industry standards are anchored by three primary pillars: procedural models like **ADDIE**, design-centric rubrics such as **Quality Matters (QM)** and **OSCQR**, and impact-oriented frameworks, most notably the **Kirkpatrick Model**.

The contemporary landscape emphasizes "Alignment"—the unified functioning of objectives, assessments, and materials—as the critical determinant of course quality. Furthermore, the integration of Artificial Intelligence (AI) and Large Language Models (LLMs) is beginning to operationalize these complex frameworks, moving the field toward "Performance-First" instructional design. This document analyzes the established rubrics, grading criteria, and the emerging role of AI in automating course assessment to inform the development of automated grading architectures.

---

## 1. Established Frameworks for Evaluating Instructional Quality

Instructional design evaluation is divided between measuring the *quality of the design* and the *effectiveness of the impact*.

### Procedural and Structural Models
*   **ADDIE (Analysis, Design, Development, Implementation, Evaluation):** The foundational lifecycle for ID. Evaluation is no longer seen as the final step but as a pervasive function. **Formative evaluation** (one-to-one, small group, and field trials) occurs during development to identify gaps, while **summative evaluation** measures terminal outcomes after implementation.
*   **Bloom’s Taxonomy:** Utilized to ensure that learning assessments align with the cognitive level of the stated objectives (e.g., testing recall vs. testing application).

### Design-Centric Rubrics
*   **Quality Matters (QM):** Considered the "gold standard" for higher education. It utilizes a peer-review system focused on research-supported standards. The QM rubric is heavily prescriptive; courses must meet all "Essential Standards" and score at least 85% to receive certification.
*   **OSCQR (SUNY Online Course Quality Review):** A flexible, non-evaluative, and open-access rubric with 50 granular standards. It is designed for formative "refresh" processes rather than summative certification and is grounded in the **Community of Inquiry (CoI)** model.
*   **OLC Course Review Scorecard (2026):** A modern evolution that evaluates both **course design** (20 indicators) and **course delivery** (15 indicators), including instructor responsiveness and engagement.

### Impact-Oriented Frameworks
*   **The Kirkpatrick Model:** The standard for measuring training effectiveness across four levels:
    1.  **Reaction:** Immediate learner response (satisfaction, relevance).
    2.  **Learning:** Acquisition of knowledge, skills, confidence, and commitment.
    3.  **Behavior:** Transfer of learning to the job environment.
    4.  **Results:** Organizational impact (ROI, productivity, safety).
*   **Phillips ROI Model:** Extends Kirkpatrick by adding a fifth level for financial cost-benefit analysis.
*   **LTEM (Learning Transfer Evaluation Model):** An 8-tier hierarchy focusing on the gap between "knowing" and "doing."

---

## 2. Key Dimensions and Criteria for Grading Courses

To be valid, an assessment of an eLearning course must score specific dimensions based on the following established criteria:

### The Cornerstone: Alignment
Alignment is achieved when the following five components work in a unified manner:
1.  **Learning Objectives:** Must be measurable and stated from the learner’s perspective.
2.  **Assessment and Measurement:** Must provide clear evidence of objective mastery.
3.  **Instructional Materials:** Must provide the information necessary to master objectives.
4.  **Learning Activities:** Must provide practice and interaction supporting objectives.
5.  **Course Technology:** Tools must facilitate learning rather than serve as an end in themselves.

### Comprehensive Quality Indicators
Beyond alignment, courses are graded on specific functional and pedagogical dimensions:

| Dimension | Key Grading Criteria |
| :--- | :--- |
| **Accessibility** | ADA/Section 508 compliance, text equivalents for images, keyboard navigation, and transcriptions for media. |
| **Usability** | Logical navigation, effective use of white space, high contrast, consistent font sizes, and lack of distracting elements (e.g., blinking text). |
| **Engagement** | Variety of activities, opportunities for learner-to-learner interaction, and "instructor presence." |
| **EdTech Quality** | The "Five Indicators": Safe (privacy), Evidence-Based, Inclusive, Usable, and Interoperable. |
| **Media Quality** | Professional presentation, clear audio/video, and appropriate timing/scaffolding of technical skills. |

---

## 3. The Role of AI in Automated Course Assessment

AI and LLMs are currently being leveraged to move evaluation from a manual, periodic task to a continuous, automated process.

*   **Benchmarking and Real-Time Feedback:** AI tools like the **OLC Course Review Assistant GPT** and **Kaddie** analyze course content against rubrics (QM, OSCQR) to provide immediate suggestions for improvement.
*   **Operationalizing the Kirkpatrick Model:** AI assistants are used to conduct performance-focused needs assessments and identify specific behaviors that will drive "Level 4 Results" during the design phase.
*   **Formative "Pulse Checks":** AI enables the launch of automated pulse surveys during a course to allow for real-time course correction, rather than waiting for end-of-course "smile sheets."
*   **Predictive Analytics:** By measuring "confidence and commitment" at Level 2, AI can act as an early predictor of whether behavior transfer (Level 3) will actually occur.

---

## 4. Architecture for a Rubric-Based AI Grading System

For an AI grading system to be valid and useful for instructional designers, its architecture must include:

*   **Alignment Matrix Analysis:** The AI must be capable of mapping objectives to assessments and materials to ensure structural integrity (the QM "Alignment" philosophy).
*   **Formative Action Planning:** Rather than a simple score, the system should produce an automated **Action Plan** (similar to the OSCQR process) to guide the designer through iterative improvements.
*   **Performance-First Design Logic:** The architecture should prompt the user to "start with the end in mind," working backward from Level 4 Results to define Level 3 Behaviors before designing content.
*   **Environment Integration:** The system should account for "Required Drivers"—the systems and management support that reinforce behavior—recognizing that design alone does not guarantee results.
*   **Interoperability Standards:** Support for **xAPI** and **Learning Record Stores (LRS)** to track learning data from multiple sources beyond simple course completions.

---

## 5. Gaps and Open Problems in Automated Assessment

Despite advancements, several challenges remain for automated AI grading:

1.  **The "Environment" Barrier:** AI can grade the *design* of a course, but it struggles to account for the learner's performance environment (manager support, tool availability, or team culture) which dictates Level 3 success.
2.  **Isolating Impact:** It remains difficult for automated systems to isolate training as the sole cause of a business result, as outcomes are influenced by parallel initiatives, leadership, and market timing.
3.  **Subjective Data Interpretation:** While AI can analyze quantitative scores, the "real gems" often lie in qualitative text feedback, which requires sophisticated sentiment and context analysis to be actionable.
4.  **Data Silos:** Many organizations lack the learning data infrastructure (beyond a basic LMS) required to provide AI with the behavioral data needed for deep Level 3 and Level 4 evaluation.

---

## Important Quotes with Context

| Quote | Source Context | Significance for AI Design |
| :--- | :--- | :--- |
| "Alignment occurs when the critical components of a course... work together in a unified manner." | *The Architecture of Quality* | Defines the primary logic the AI must use to "grade" a course's validity. |
| "A high satisfaction score does not mean people learned anything... and it says nothing about whether the business is better off." | *Kirkpatrick Model (Valamis)* | Highlights the risk of AI focusing on "Level 1" metrics (smile sheets) over impact. |
| "The model's greatest strength is its simplicity and flexibility... adaptable across industries." | *The Kirkpatrick Model (Partners)* | Suggests AI tools should remain industry-agnostic but sector-aware. |
| "Level 3 evaluation should look at both the learner and the context they work in." | *Kirkpatrick Model (Valamis)* | Warns that AI grading must eventually factor in "Performance Environment" to be accurate. |

---

## Actionable Insights for AI Assistant Architecture

*   **Design for Iteration, Not Just Certification:** Frame the AI’s output as a professional development exercise rather than a punitive quality assurance procedure. Use the "formative" approach of OSCQR.
*   **Prioritize Accessibility from Step One:** Integrate accessibility standards (Standard 8 in QM, Standards 34-37 in OSCQR) as non-negotiable grading criteria to ensure inclusive design.
*   **Implement "Leading Indicators":** Program the AI to identify short-term observations (e.g., specific quiz patterns or engagement data) that suggest long-term business results are on track.
*   **Focus on Measurability:** If the AI cannot identify a measurable objective (the QM "Cornerstone"), it should refuse to grade the alignment of other course components.
*   **Reverse-Engineer Strategy:** Build a module that requires users to define Level 4 Results *before* they are allowed to upload course materials for grading, ensuring the design is performance-driven.