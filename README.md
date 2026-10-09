# Conversation Compressor Tool (`conversation-compressor-tool`)

## Description

The Conversation Compressor Tool is a utility designed to manage and optimize the AI Agent's memory and context usage over prolonged interactions. Its primary function is to provide a callable mechanism that allows the AI model to proactively initiate conversation compaction when the token usage of the current session approaches a predefined threshold.

## Core Functionality

This tool acts as an interface to a hypothetical backend memory or context service. It does not perform the compaction itself but instead signals to the system that a compaction action is required to maintain context relevance while preventing token overload.

### Tool Signature: `setCompactionLimit`

The primary method of the tool is `setCompactionLimit`.

**Parameters:**
*   `targetPercentage` (Number): The target token usage percentage (a value between 0.0 and 1.0) at which the conversation compaction process should be triggered.

**Example Usage (Conceptual call from AI Agent):**
`setCompactionLimit({ targetPercentage: 0.7 })`

**Effect:**
When invoked, this method configures the system to trigger a compaction process once the token usage reaches the specified `targetPercentage`.

## Implementation Notes

This tool is implemented as a host-side Tool within the Cordis framework.

**Note on Current State:**
The provided code serves as the structural definition for the plugin. In a full production implementation, the logic within `setCompactionLimit` would need to be expanded to interface with the specific service responsible for context management (e.g., triggering abstractive summarization or context pruning based on the configured percentage).

## Installation

*(This section should be customized based on how the plugin is hosted)*

This plugin must be packaged as a Cordis Bundle and installed into the current Harness profile to be made available to the AI Agent.
